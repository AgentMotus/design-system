---
name: brand-system
description: Apply MotusDAO’s canonical brand tokens and implementation rules (colors, typography, spacing, glassmorphism, gradients, motion, accessibility) when building or reviewing UI, landing pages, social assets, and templates.
---

# MotusDAO Brand System Skill

Use this skill whenever the user asks for design updates, UI polishing, landing pages, visual consistency, template creation, token cleanup, or brand-system migration.

## Source of Truth
- `docs/04-design-system-operativo.md`
- `docs/03-manual-identidad-marca-v1.md`

If there is a conflict, prefer the operational tokens in doc 04 and enforce brand prohibitions from doc 03.

---

## 1) Canonical Design Tokens

### Color Tokens
```css
:root {
  --brand-purple: #9333EA;
  --brand-pink: #EC4899;
  --brand-blue: #6366F1;
  --brand-cyan: #00E5FF;
  --brand-magenta: #E144FF;

  --bg-primary: #000000;
  --bg-elevated: #0B101A;
  --bg-surface: rgba(255, 255, 255, 0.06);
  --bg-surface-hover: rgba(255, 255, 255, 0.10);

  --text-primary: rgba(255, 255, 255, 0.9);
  --text-secondary: rgba(255, 255, 255, 0.6);
  --text-muted: rgba(255, 255, 255, 0.4);

  --border-default: rgba(255, 255, 255, 0.10);
  --border-strong: rgba(255, 255, 255, 0.20);

  --success: #22C55E;
  --warning: #F59E0B;
  --error: #EF4444;
  --info: #6366F1;
}
```

### Gradient Tokens
```css
:root {
  --grad-brand: linear-gradient(to right, #9333EA, #EC4899);
  --grad-cool: linear-gradient(to right, #6366F1, #06B6D4);
  --grad-holo: linear-gradient(135deg, #00E5FF, #E144FF, #A7B4C6);
  --grad-subtle: radial-gradient(circle at 30% 30%, rgba(147,51,234,0.15), transparent 50%);

  --grad-bg-ambient:
    radial-gradient(60% 60% at 20% 20%, rgba(99, 102, 241, 0.18), transparent 60%),
    radial-gradient(60% 60% at 80% 30%, rgba(236, 72, 153, 0.16), transparent 60%),
    radial-gradient(70% 70% at 50% 80%, rgba(147, 51, 234, 0.18), transparent 60%);
}
```

### Glassmorphism Tokens
```css
:root {
  --glass-bg: linear-gradient(135deg, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0.05) 100%);
  --glass-border: rgba(255, 255, 255, 0.15);
  --glass-blur: 20px;
  --glass-blur-strong: 32px;

  --shadow-glass: 0 8px 32px rgba(0, 0, 0, 0.15), 0 0 20px rgba(255, 255, 255, 0.08);
  --shadow-glow: 0 0 20px rgba(147, 51, 234, 0.3);
  --shadow-glow-cyan: 0 0 20px rgba(0, 229, 255, 0.3);
  --shadow-soft: 0 4px 20px rgba(0, 0, 0, 0.1);
}
```

### Typography Tokens
```css
:root {
  --font-body: 'Inter', sans-serif;
  --font-heading: 'Jura', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
  --font-display: 'Orbitron', monospace; /* Psychat display only */

  --text-display: clamp(2.5rem, 5vw, 4rem);
  --text-h1: clamp(2rem, 4vw, 3rem);
  --text-h2: clamp(1.5rem, 3vw, 2.25rem);
  --text-h3: clamp(1.25rem, 2.5vw, 1.75rem);
  --text-h4: 1.125rem;
  --text-body-lg: 1.125rem;
  --text-body: 1rem;
  --text-body-sm: 0.875rem;
  --text-caption: 0.75rem;

  --leading-tight: 1.1;
  --leading-snug: 1.3;
  --leading-normal: 1.6;
  --leading-relaxed: 1.75;
}
```

### Spacing / Radius / Motion
```css
:root {
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-6: 24px;
  --space-8: 32px;
  --space-12: 48px;
  --space-16: 64px;
  --space-24: 96px;

  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 24px;
  --radius-full: 9999px;

  --ease-default: cubic-bezier(0.4, 0, 0.2, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --duration-fast: 150ms;
  --duration-normal: 300ms;
  --duration-slow: 500ms;
  --duration-ambient: 6s;
}
```

### Font Import
```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&family=Jura:wght@500;600;700&family=Orbitron:wght@600;700&display=swap');
```

---

## 2) Product-Specific Overrides

### Hub
- Uses unified tokens as-is.
- Matrix mode optional only:
  - `--matrix-text: #39FF14`
  - `--matrix-accent: #00FF41`
  - sharp corners allowed only in Matrix mode.

### Psychat
- `--color-primary: var(--brand-cyan)`
- `--color-accent: var(--brand-magenta)`
- `--bg-primary: var(--bg-elevated)`
- Orbitron for hero display text.
- Terminal elements in JetBrains Mono with cyan glow.
- Psychat-only animations (`neon-flicker`, `holographic-scan`, etc.) must not leak into Hub/main site.

### Main Site
- Purple→pink is primary visual accent.
- No cyan/terminal styling in normal brand moments.
- Dark nav/footer mandatory.

---

## 3) Mandatory Rules

1. Dark-mode-first across products (except intentional light sections on main site).
2. Minimum body text: **16px**.
3. Glass cards = surface + blur + border (don’t fake with opaque flat blocks).
4. Use spacing scale (4px grid). No random spacing.
5. Max 2 gradients per viewport.
6. Respect accessibility: WCAG AA (4.5:1 body, 3:1 large text).
7. CTA copy format: verb + noun (e.g., “Request Demo”, “Start Session”).
8. Claims must be verifiable; no hype language.

---

## 4) Hard Prohibitions

- No orange/coral accents (legacy error).
- No Playfair Display or Share Tech Mono.
- No savior framing (“saving mental health”).
- No “revolutionary/disruptive/innovative” fluff without specifics.
- No stock-photo cliches.
- Do not call Cyrene an “AI therapist” (it is an AI assistant).

---

## 5) Implementation Checklist

When producing design/code, always return:
- Token mapping used (colors/fonts/spacing/radius/motion)
- Which product mode is targeted (Hub/Psychat/Main)
- Accessibility notes (contrast + min text sizes)
- Any override justification

If user-provided values conflict with this skill, call out the conflict explicitly and propose a compliant alternative.
