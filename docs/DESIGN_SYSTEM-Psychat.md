# PsyChat Holographic Design System

A portable design system for holographic, terminal-style UIs. Use this document in any project (PolkaPsychat, PsyChat, or new apps) to keep visuals consistent.

**Source:** Derived from PolkaPsychat `DESIGN_SYSTEM_PROMPT.md` (main).  
**How to propagate:** Copy this file into your repo (e.g. `docs/DESIGN_SYSTEM.md` or project root) and reference it when building UI.

---

## 1. Design Tokens & CSS Variables

### Core Color Palette

```css
:root {
  /* Primary Colors */
  --color-bg: #0B101A;
  --color-primary: #00E5FF;
  --color-accent: #E144FF;
  --color-secondary: #9D68FF;
  --color-surface: rgba(255,255,255,0.06);
  --color-text: rgba(255,255,255,0.9);
  
  /* Holographic Glass System */
  --bg-dark: #05070D;
  --bg-panel: rgba(255,255,255,0.05);
  --cyan: #00E5FF;
  --lavender: #E144FF;
  --silver: #A7B4C6;
  --neon-blue: rgba(0,229,255,0.35);
  --neon-purple: rgba(225,68,255,0.25);
  --holo-gradient: linear-gradient(135deg, var(--cyan), var(--lavender), var(--silver));
  
  /* Enhanced Holographic */
  --electric-cyan: #00FFFF;
  --vibrant-magenta: #FF00FF;
  --deep-black: #000000;
  --translucent-white: rgba(255, 255, 255, 0.15);
  
  /* Depth-based opacity */
  --opacity-bg: 0.05;
  --opacity-far: 0.15;
  --opacity-mid: 0.20;
  --opacity-near: 0.25;
  --opacity-main: 0.30;
  
  /* Blur & Radius */
  --blur: 20px;
  --radius: 12px;
}
```

### Typography

```css
:root {
  --font-display: 'Orbitron', monospace;      /* Headlines, hero */
  --font-heading: 'JetBrains Mono', monospace; /* Section headings */
  --font-mono: 'JetBrains Mono', monospace;   /* Terminal, code, UI */
  --font-body: 'Inter', sans-serif;           /* Body text */
  --font-special: 'Jura', sans-serif;         /* Special accents */
}

@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:ital,wght@0,100..800;1,100..800&family=Orbitron:wght@400;500;600;700;800;900&family=Jura:wght@300;400;500;600;700&display=swap');
```

### Z-Index

```css
:root {
  --z-background-deep: -20;
  --z-background-mid: -10;
  --z-background-overlay: -5;
  --z-content: 0;
  --z-content-elevated: 10;
  --z-modal: 50;
  --z-loader: 100;
}
```

---

## 2. Core Animations

```css
@keyframes holo-glow {
  0% { opacity: 0.5; transform: translateX(-10%); }
  50% { opacity: 1; transform: translateX(10%); }
  100% { opacity: 0.5; transform: translateX(-10%); }
}

@keyframes holographic-scan {
  0% { transform: translateY(-100%) rotateX(0deg); opacity: 0; }
  50% { transform: translateY(0%) rotateX(0deg); opacity: 1; }
  100% { transform: translateY(100%) rotateX(0deg); opacity: 0; }
}

@keyframes circuit-pulse {
  0%, 100% { opacity: 0.3; transform: scale(1); }
  50% { opacity: 0.8; transform: scale(1.02); }
}

@keyframes neon-flicker {
  0%, 100% { opacity: 1; filter: brightness(1); }
  2% { opacity: 0.8; filter: brightness(1.2); }
  4% { opacity: 1; filter: brightness(0.9); }
  6% { opacity: 0.9; filter: brightness(1.1); }
  8% { opacity: 1; filter: brightness(1); }
}

@keyframes float-panel {
  0%, 100% { transform: translateY(0px) rotateZ(0deg); }
  25% { transform: translateY(-8px) rotateZ(0.5deg); }
  50% { transform: translateY(-4px) rotateZ(0deg); }
  75% { transform: translateY(-12px) rotateZ(-0.5deg); }
}

@keyframes edge-glow-pulse {
  0%, 100% { box-shadow: 0 0 20px rgba(0, 255, 255, 0.3), 0 0 40px rgba(0, 255, 255, 0.2), inset 0 1px 0 rgba(255, 255, 255, 0.2); }
  50% { box-shadow: 0 0 30px rgba(0, 255, 255, 0.5), 0 0 60px rgba(0, 255, 255, 0.3), inset 0 1px 0 rgba(255, 255, 255, 0.3); }
}
```

**Utility classes:** `.neon-flicker`, `.circuit-pulse`, `.float-panel`, `.holographic-scan`

---

## 3. Color Usage

| Role | Color | Use |
|------|--------|-----|
| Primary | Cyan `#00E5FF` | Actions, active states, system messages |
| Accent | Magenta `#E144FF` | AI, highlights, secondary actions |
| Secondary | Purple `#9D68FF` | Network status, tertiary elements |
| Text | White 90% | Body content |
| Terminal/system | Cyan-300 | Terminal output, system messages |
| AI/special | Fuchsia-300 | AI responses, notifications |
| Muted | White 60–70% | Secondary text, timestamps |
| Background | `#0B101A` | Base; panels use `rgba(0,0,0,0.2–0.3)` + backdrop-blur |

---

## 4. Typography Classes

```css
.terminal-text {
  font-family: var(--font-mono);
  color: rgba(255, 255, 255, 0.9);
  text-shadow: 0 0 6px rgba(0, 229, 255, 0.6);
}

.display-text {
  font-family: var(--font-display);
  color: var(--color-primary);
  text-shadow: 0 0 15px rgba(0, 229, 255, 0.8);
}

.body-text {
  font-family: var(--font-body);
  color: var(--color-text);
}

.special-text {
  font-family: var(--font-special);
  color: var(--color-accent);
}
```

---

## 5. Glass & Border Effects

```css
.holo-glass {
  background: linear-gradient(135deg, rgba(0, 229, 255, 0.1) 0%, rgba(225, 68, 255, 0.05) 50%, rgba(167, 180, 198, 0.1) 100%);
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 0 30px rgba(0, 229, 255, 0.3), inset 0 1px 0 rgba(255, 255, 255, 0.2), inset 0 -1px 0 rgba(0, 0, 0, 0.3);
}

.neon-solid-cyan {
  color: #00E5FF;
  text-shadow: 0 0 10px rgba(0, 229, 255, 0.8), 0 0 20px rgba(0, 229, 255, 0.6), 0 0 30px rgba(0, 229, 255, 0.4);
}

.neon-solid-magenta {
  color: #E144FF;
  text-shadow: 0 0 10px rgba(225, 68, 255, 0.8), 0 0 20px rgba(225, 68, 255, 0.6), 0 0 30px rgba(225, 68, 255, 0.4);
}
```

---

## 6. Layout & Spacing

**Containers:**

- Max width: `1440px`, center with `mx-auto`, padding `px-4 py-8` / `lg:px-8`.
- Grid: `grid-cols-1 lg:grid-cols-12`, typical splits `lg:col-span-4` / `lg:col-span-8`.

**Spacing scale:** xs 8px, sm 12px, md 16px, lg 24px, xl 32px, 2xl 48px.

---

## 7. Tailwind Extensions (optional)

Add to `tailwind.config.js` if using Tailwind:

```javascript
theme: {
  extend: {
    fontFamily: {
      display: ['Orbitron', 'monospace'],
      heading: ['JetBrains Mono', 'monospace'],
      mono: ['JetBrains Mono', 'monospace'],
      body: ['Inter', 'sans-serif'],
      special: ['Jura', 'sans-serif'],
    },
    colors: {
      primary: 'var(--color-primary)',
      accent: 'var(--color-accent)',
      secondary: 'var(--color-secondary)',
      surface: 'var(--color-surface)',
      'electric-cyan': '#00FFFF',
      'vibrant-magenta': '#FF00FF',
    },
    boxShadow: {
      'holo-glow': '0 0 20px rgba(0, 255, 255, 0.4), 0 0 40px rgba(255, 0, 255, 0.3)',
      'holo-glow-magenta': '0 0 20px rgba(255, 0, 255, 0.3), 0 0 40px rgba(255, 0, 255, 0.2)',
    },
    animation: {
      'edge-glow-pulse': 'edge-glow-pulse 4s ease-in-out infinite',
      'holographic-scan': 'holographic-scan 6s linear infinite',
    },
  },
}
```

---

## 8. Component Patterns (React + Framer Motion)

**Holographic background (concept):**

- Base: `bg-gradient-radial from-cyan-500/20 via-transparent to-fuchsia-500/20`.
- Animated radial gradients (positions 20%/80% swapping).
- Blur orbs (cyan/fuchsia) with slow x/y/scale animation.
- Optional thin scan line (gradient line animating top→bottom).

**Panels:**

- `rounded-2xl backdrop-blur-xl border border-cyan-400/20 bg-black/20` (or `bg-black/30` elevated).
- Inner borders: `border-white/10`, `border-white/5` for depth.
- Optional scan-line overlay with `holographic-scan` animation.

**Buttons:**

- Primary: gradient `from-cyan-500/20 to-fuchsia-500/20`, border `border-cyan-400/30`, text `text-cyan-300`, hover glow `hover:shadow-[0_0_20px_rgba(0,255,255,0.3)]`.
- Secondary: swap cyan/fuchsia order and border/text to fuchsia.
- Ghost: transparent bg, `border-white/20`, hover `bg-white/5`.

**Terminal text:**

- Prompt: `font-mono text-cyan-400 text-xs neon-flicker`.
- Output: `font-mono text-cyan-300` or `text-fuchsia-300` / `text-slate-300` + `neon-flicker` and optional `drop-shadow-[0_0_6px_...]`.

**Motion:**

- Page: `initial={{ opacity: 0 }}` → `animate={{ opacity: 1 }}`, duration ~0.8s.
- Cards: `initial={{ opacity: 0, scale: 0.98, y: 10 }}` → `animate={{ opacity: 1, scale: 1, y: 0 }}`, optional `whileHover={{ scale: 1.02, boxShadow: "0 0 20px rgba(0,255,255,0.3)" }}`.

---

## 9. Do's and Don'ts

**Do:**

- Use design tokens (CSS variables) for colors.
- Use `backdrop-blur-xl` for glass panels.
- Use `font-mono` for terminal/code text.
- Apply `neon-flicker` to terminal-style copy.
- Keep panel opacity via tokens (e.g. ≤ 0.3).
- Use the z-index scale for stacking.

**Don't:**

- Hardcode hex/rgba outside tokens.
- Use solid flat backgrounds; prefer glass/blur.
- Skip the holographic background pattern where the product is “terminal/holo”.
- Mix font roles without a clear purpose.
- Use panel opacity above token limits.

---

## 10. Quick Reference

**Terminal line:**  
`className="font-mono text-xs text-cyan-300 neon-flicker"`

**Panel:**  
`className="rounded-2xl backdrop-blur-xl border border-cyan-400/20 bg-black/20 p-4"`

**Primary button:**  
`className="px-4 py-2 rounded-xl bg-gradient-to-r from-cyan-500/20 to-fuchsia-500/20 border border-cyan-400/30 text-cyan-300 hover:shadow-[0_0_20px_rgba(0,255,255,0.3)] transition-all"`

**Background:**  
`className="absolute inset-0 bg-gradient-radial from-cyan-500/20 via-transparent to-fuchsia-500/20"`

---

## Propagation Checklist

When adding this design system to a new project:

1. Copy this `.md` into the repo (e.g. `docs/DESIGN_SYSTEM.md`).
2. Add the CSS variables (Section 1) to global styles or a design-tokens file.
3. Add keyframes and utility classes (Sections 2, 4, 5) or map them in Tailwind.
4. If using Tailwind, extend config (Section 7).
5. Implement or copy HoloPanel / HoloButton / HoloText (or equivalents) from PolkaPsychat if you use React.
6. Point contributors and AI to this file for UI consistency.
