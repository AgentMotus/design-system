# 04 — Design System Operativo / Operational Design System

**Version:** 1.0  
**Date:** 2026-02-27  
**Purpose:** Unified tokens and template specs that replace the separate Hub and Psychat systems.

---

## 1. Unified Design Tokens

These tokens supersede individual values in `DESIGN_SYSTEM-HUB.md` and `DESIGN_SYSTEM-Psychat.md`. Both products should migrate to these shared tokens.

### 1.1 Color Tokens

```css
:root {
  /* === Brand === */
  --brand-purple: #9333EA;
  --brand-pink: #EC4899;
  --brand-blue: #6366F1;
  --brand-cyan: #00E5FF;
  --brand-magenta: #E144FF;

  /* === Neutrals === */
  --bg-primary: #000000;
  --bg-elevated: #0B101A;
  --bg-surface: rgba(255, 255, 255, 0.06);
  --bg-surface-hover: rgba(255, 255, 255, 0.10);
  --text-primary: rgba(255, 255, 255, 0.9);
  --text-secondary: rgba(255, 255, 255, 0.6);
  --text-muted: rgba(255, 255, 255, 0.4);
  --border-default: rgba(255, 255, 255, 0.10);
  --border-strong: rgba(255, 255, 255, 0.20);

  /* === Semantic === */
  --success: #22C55E;
  --warning: #F59E0B;
  --error: #EF4444;
  --info: #6366F1;

  /* === Gradients === */
  --grad-brand: linear-gradient(to right, #9333EA, #EC4899);
  --grad-cool: linear-gradient(to right, #6366F1, #06B6D4);
  --grad-holo: linear-gradient(135deg, #00E5FF, #E144FF, #A7B4C6);
  --grad-bg-ambient: radial-gradient(60% 60% at 20% 20%, rgba(99, 102, 241, 0.18), transparent 60%),
    radial-gradient(60% 60% at 80% 30%, rgba(236, 72, 153, 0.16), transparent 60%),
    radial-gradient(70% 70% at 50% 80%, rgba(147, 51, 234, 0.18), transparent 60%);

  /* === Glass === */
  --glass-bg: linear-gradient(135deg, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0.05) 100%);
  --glass-border: rgba(255, 255, 255, 0.15);
  --glass-blur: 20px;
  --glass-blur-strong: 32px;

  /* === Spacing (4px grid) === */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-6: 24px;
  --space-8: 32px;
  --space-12: 48px;
  --space-16: 64px;
  --space-24: 96px;

  /* === Radius === */
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 24px;
  --radius-full: 9999px;

  /* === Shadows === */
  --shadow-glass: 0 8px 32px rgba(0, 0, 0, 0.15), 0 0 20px rgba(255, 255, 255, 0.08);
  --shadow-glow: 0 0 20px rgba(147, 51, 234, 0.3);
  --shadow-glow-cyan: 0 0 20px rgba(0, 229, 255, 0.3);
  --shadow-soft: 0 4px 20px rgba(0, 0, 0, 0.1);

  /* === Motion === */
  --ease-default: cubic-bezier(0.4, 0, 0.2, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --duration-fast: 150ms;
  --duration-normal: 300ms;
  --duration-slow: 500ms;
  --duration-ambient: 6s;
}
```

### 1.2 Typography Tokens

```css
:root {
  --font-body: 'Inter', sans-serif;
  --font-heading: 'Jura', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
  --font-display: 'Orbitron', monospace; /* Psychat only */

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

### 1.3 Tailwind Config (unified)

```javascript
// tailwind.config.js — shared across all products
module.exports = {
  theme: {
    extend: {
      colors: {
        brand: {
          purple: '#9333EA',
          pink: '#EC4899',
          blue: '#6366F1',
          cyan: '#00E5FF',
          magenta: '#E144FF',
        },
        surface: 'rgba(255,255,255,0.06)',
        'surface-hover': 'rgba(255,255,255,0.10)',
        success: '#22C55E',
        warning: '#F59E0B',
        error: '#EF4444',
      },
      fontFamily: {
        sans: ['Inter', 'sans-serif'],
        heading: ['Jura', 'sans-serif'],
        mono: ['JetBrains Mono', 'monospace'],
        display: ['Orbitron', 'monospace'],
      },
      borderRadius: {
        sm: '8px',
        md: '12px',
        lg: '16px',
        xl: '24px',
      },
      backdropBlur: {
        glass: '20px',
        'glass-strong': '32px',
      },
      boxShadow: {
        glass: '0 8px 32px rgba(0,0,0,0.15), 0 0 20px rgba(255,255,255,0.08)',
        glow: '0 0 20px rgba(147,51,234,0.3)',
        'glow-cyan': '0 0 20px rgba(0,229,255,0.3)',
        soft: '0 4px 20px rgba(0,0,0,0.1)',
      },
      animation: {
        'fade-in': 'fadeIn 0.5s ease-in-out',
        'slide-up': 'slideUp 0.5s ease-out',
        float: 'float 6s ease-in-out infinite',
        'pulse-glow': 'pulseGlow 2s ease-in-out infinite alternate',
      },
    },
  },
};
```

### 1.4 Font Import (single line for all products)

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&family=Jura:wght@500;600;700&family=Orbitron:wght@600;700&display=swap');
```

---

## 2. Product-Specific Overrides

### Hub
Uses full unified system as-is. Matrix theme remains as an optional fun mode with these additions:
- `--matrix-text: #39FF14`
- `--matrix-accent: #00FF41`
- Sharp corners (`border-radius: 0`) in Matrix mode only

### Psychat
Extends unified system with:
- Primary color override: `--color-primary: var(--brand-cyan)`
- Accent: `--color-accent: var(--brand-magenta)`
- Background: `--bg-primary: var(--bg-elevated)` (#0B101A)
- Additional animations: `neon-flicker`, `holographic-scan`, `float-panel`, `edge-glow-pulse`
- Display font: Orbitron for hero headings
- Terminal elements: JetBrains Mono with cyan text-shadow

### Main Site
Uses unified system with:
- May use light backgrounds for specific sections (hero, course cards) but navigation and footer must be dark
- No cyan, no terminal aesthetic
- Purple-pink gradient as primary

---

## 3. Template Specifications

### Template 1: X Post (1:1 — 1080×1080px)

```
┌────────────────────────────────┐
│ bg: #000000                    │
│                                │
│ ┌────────────────────────────┐ │
│ │  [glass card, 40px pad]    │ │
│ │                            │ │
│ │  Headline: Jura 700        │ │
│ │  48-60px, white or grad    │ │
│ │  max 3 lines               │ │
│ │                            │ │
│ │  Body: Inter 400           │ │
│ │  24px, text-secondary      │ │
│ │  max 2 lines               │ │
│ │                            │ │
│ │  [metric or screenshot]    │ │
│ │                            │ │
│ └────────────────────────────┘ │
│                                │
│ MotusDAO logo ──── bottom-right│
│ 32px from edges                │
└────────────────────────────────┘
```

- **Background:** Solid black + 1-2 ambient gradient radials (low opacity)
- **Card:** Glass panel, `--radius-xl`, `--glass-border`
- **Typography:** Headline in Jura, body in Inter
- **Logo:** Primary logomark, 40px, bottom-right with 32px margin
- **Optional:** Gradient border on card, metric callout in gradient text

### Template 2: X Vertical (9:16 — 1080×1920px)

```
┌────────────────────┐
│ bg: #000000        │
│                    │
│ Logo + "MotusDAO"  │ ← top-left, 24px margin
│                    │
│                    │
│ Headline: Jura 700 │
│ 56-72px, gradient  │
│ text, centered     │
│                    │
│ ─── divider ───    │ ← 1px grad-brand line
│                    │
│ Body: Inter 400    │
│ 28px, centered     │
│ max 4 lines        │
│                    │
│                    │
│ [screenshot or     │
│  visual element]   │
│                    │
│                    │
│ CTA text: Inter 600│
│ 24px, brand-cyan   │
│                    │
│ @motusdao          │ ← bottom-center, caption
└────────────────────┘
```

### Template 3: Landing Hero (full-width, 100vh)

```
┌──────────────────────────────────────────────────┐
│ bg: --bg-primary + --grad-bg-ambient             │
│                                                  │
│ [nav bar — glass, logo left, links right]        │
│                                                  │
│         H1: Jura 700, --text-display             │
│         gradient text, max-w-720px, centered     │
│                                                  │
│         Subhead: Inter 400, --text-body-lg       │
│         text-secondary, max-w-560px              │
│                                                  │
│     [Primary CTA]      [Ghost CTA]              │
│                                                  │
│     ┌─────┐  ┌─────┐  ┌─────┐  ┌─────┐         │
│     │ met │  │ met │  │ met │  │ met │          │ ← proof strip
│     └─────┘  └─────┘  └─────┘  └─────┘         │
│                                                  │
└──────────────────────────────────────────────────┘
```

- Full viewport height, vertically centered content
- Ambient gradient background, optionally animated (8s shift)
- Trust/proof strip at bottom: 3-4 metric cards in a row

### Template 4: Proof Card (400×240px or flexible)

```
┌─────────────────────────┐
│ glass panel              │
│                          │
│  [icon: Lucide, 24px]    │
│                          │
│  Metric: Jura 700        │
│  36px, gradient text     │
│  e.g. "1,247"            │
│                          │
│  Label: Inter 400        │
│  14px, text-secondary    │
│  e.g. "Active Sessions"  │
│                          │
└─────────────────────────┘
```

- Hover: `translateY(-2px)`, `shadow-glow`
- On dark background only
- Metrics must be verifiable (link to source or on-chain data)

### Template 5: Partnership Announcement (1200×675px / OG image)

```
┌──────────────────────────────────────────┐
│ bg: #000000 + subtle grad-brand radials  │
│                                          │
│  [Partner Logo]    ×    [MotusDAO Logo]  │
│       centered, 64px height each         │
│                                          │
│  "MotusDAO × Partner Name"              │
│  Jura 600, 36px, white                  │
│                                          │
│  One-line description                    │
│  Inter 400, 20px, text-secondary         │
│                                          │
│  ─── gradient divider ───                │
│                                          │
│  motusdao.org                            │
│  Inter 400, 16px, brand-cyan             │
│                                          │
└──────────────────────────────────────────┘
```

- Partner logo: request SVG/PNG with transparent background
- If partner has a light logo, place on glass card; if dark-friendly, place directly
- No "We're excited to announce" — just state the partnership and what it does

---

## 4. Migration Notes

### From DESIGN_SYSTEM-HUB.md
- Replace `--primary-black`, `--primary-blue`, `--primary-gray` → unified tokens
- Replace `--grad-primary` → `--grad-brand`
- Drop Playfair Display, Share Tech Mono from font imports
- Keep Matrix theme as optional overlay (existing implementation is fine)
- Map `font-sans` → `--font-body`, `font-heading` → `--font-heading`, `font-matrix` → `--font-mono`

### From DESIGN_SYSTEM-Psychat.md
- Replace `--color-bg` → `--bg-elevated`
- Replace `--color-primary` → `--brand-cyan`
- Replace `--color-accent` → `--brand-magenta`
- Replace `--color-secondary` → `--brand-blue`
- Keep holographic animations, but they're Psychat-scoped (don't export to Hub)
- `--font-heading` in Psychat context = JetBrains Mono (keep for section headings); hero display = Orbitron
- Psychat body text should use Inter (not JetBrains Mono) for readability
