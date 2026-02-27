# 03 — Manual de Identidad de Marca v1 / Brand Identity Manual

**MotusDAO — AI-Human Hybrid Mental Health Infrastructure**  
**Version:** 1.0  
**Date:** 2026-02-27

---

## Table of Contents

1. [Brand Core](#1-brand-core)
2. [Voice & Tone](#2-voice--tone)
3. [Messaging System](#3-messaging-system)
4. [Visual System](#4-visual-system)
5. [Logo Usage](#5-logo-usage)
6. [Component Rules](#6-component-rules)
7. [Accessibility](#7-accessibility)
8. [Do / Don't](#8-do--dont)
9. [Brand QA Checklist](#9-brand-qa-checklist)

---

## 1. Brand Core

### Purpose
Build decentralized infrastructure that gives people sovereignty over their mental health data while connecting them with AI-augmented, human-led care.

### Promise
Your therapy, your data, your terms. We ship infrastructure — not promises.

### Personality Traits
| Trait | Expression |
|-------|-----------|
| **Technical** | We show architecture, not buzzwords. We cite specifics. |
| **Grounded** | No hype, no savior tone. We describe what exists and what's next. |
| **Human** | Technology serves the therapeutic relationship, never replaces it. |
| **Sovereign** | Privacy and self-custody aren't features — they're the foundation. |
| **Relentless** | We ship weekly. Roadmap is a log, not a wish list. |

### Brand Archetype
**The Builder** (Creator archetype, Web3 inflection) — Builds systems that outlast their creators. Not a hero rescuing anyone; an engineer constructing infrastructure others can build on.

### Brand Essence (one line)
> Execution-first hyperstructure for mental health sovereignty.

---

## 2. Voice & Tone

### Core Voice Attributes
- **Direct** — Short sentences. Active voice. No filler.
- **Technical but accessible** — Use precise terms, then explain once. Don't dumb down; don't gatekeep.
- **Confident, not arrogant** — State what we've built. Don't claim what we haven't.
- **Warm in care contexts, sharp in protocol contexts** — Psychat copy can be gentler. Tokenomics copy should be precise.

### Channel-Specific Rules

#### X / Twitter
- Max 240 chars per idea (leave room for engagement)
- Lead with the build, not the vision: "Shipped X" > "We believe in X"
- Threads: open with a hook (metric or screenshot), close with a CTA
- Allowed: technical jargon, emojis (sparingly: 🔧 🧠 ⚡ 🏗️), metrics
- Prohibited: "🚀 to the moon", "WAGMI", "we're changing the world"

#### Landing Pages (motusdao.org)
- Hero: one sentence max. Subhead: one sentence max. Then CTA.
- Section headings: action-oriented ("Connect with a therapist" not "Our services")
- Social proof before CTA when possible
- No walls of text — use cards, bullets, visuals

#### Email / Newsletter
- Subject line: specific, not clickbait ("Hub v2.3: smart wallet payments live")
- Body: 3 paragraphs max. Link to detail.
- Sign-off: "— MotusDAO team" (not individual names unless relevant)

#### Telegram / Community
- Casual but informed. Answer questions directly.
- Share builds, screenshots, metrics
- Avoid financial advice or token price discussion
- Pin important updates. Don't flood.

---

## 3. Messaging System

### Messaging Pillars

| Pillar | Core Message | Supporting Points |
|--------|-------------|-------------------|
| **Sovereignty** | You own your mental health data | Self-custody, encryption, no platform lock-in, data portability |
| **Hybrid Care** | AI augments human therapists — never replaces them | Cyrene AI for 24/7 support, human therapists for deep work, seamless handoff |
| **Infrastructure** | We build the rails, not just the app | Open protocol, composable, hyperstructure that outlasts MotusDAO itself |
| **Execution** | Working code > whitepapers | Live dapp, active users, shipping cadence, transparent treasury |
| **Dataconomy** | Your data has value — you should capture it | Patient-controlled data marketplace, ethical monetization, privacy-preserving analytics |

### Allowed Claims
- ✅ "Self-custody of therapy data"
- ✅ "AI-human hybrid model"
- ✅ "Live on [specific chain]"
- ✅ "X active users / Y sessions completed" (with verifiable source)
- ✅ "Open-source [component]" (if actually open source)
- ✅ "End-to-end encrypted"

### Prohibited Claims
- ❌ "We're saving mental health" / "We're revolutionizing therapy"
- ❌ "The future of mental health" (unless qualified with specifics)
- ❌ Any medical claims ("MotusDAO treats depression")
- ❌ Token price predictions or financial advice
- ❌ "Decentralized" for components that aren't actually decentralized
- ❌ "AI therapist" — Cyrene is an AI assistant, not a licensed therapist
- ❌ Comparisons that disparage specific competitors by name

### Message Examples

**Good:**
> "Psychat v3 ships E2E encrypted sessions on Solana. Your therapist sees your notes. We don't."

**Bad:**
> "We're revolutionizing mental healthcare by bringing the power of blockchain to therapy! 🚀"

**Good:**
> "Hub payments: USDC → therapist wallet in <10 seconds. No intermediary. No 30% platform fee."

**Bad:**
> "Our innovative payment system disrupts the traditional healthcare payment paradigm."

---

## 4. Visual System

### 4.1 Color Palette

#### Primary Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--brand-purple` | `#9333EA` | Primary brand, gradients, CTAs |
| `--brand-pink` | `#EC4899` | Gradient endpoints, accents |
| `--brand-blue` | `#6366F1` | Secondary actions, links |
| `--brand-cyan` | `#00E5FF` | Psychat primary, terminal accents |

#### Neutral Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-primary` | `#000000` | Default background (dark mode) |
| `--bg-secondary` | `#0B101A` | Psychat background, elevated dark |
| `--bg-surface` | `rgba(255,255,255,0.06)` | Cards, panels |
| `--text-primary` | `rgba(255,255,255,0.9)` | Body text (dark mode) |
| `--text-secondary` | `rgba(255,255,255,0.6)` | Muted text |
| `--border-default` | `rgba(255,255,255,0.1)` | Card borders, dividers |

#### Semantic Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--success` | `#22C55E` | Active status, confirmations |
| `--warning` | `#F59E0B` | Pending, attention |
| `--error` | `#EF4444` | Errors, destructive actions |
| `--info` | `#6366F1` | Informational |

#### Product Accent Allowances
- **Hub:** Full palette. Purple-pink gradients as primary.
- **Psychat:** Cyan (`#00E5FF`) as primary, magenta (`#E144FF`) as accent. Must still use shared neutrals and brand purple in navigation/footer.
- **Main site:** Purple-pink as primary. No orange/coral — this was a legacy error.

### 4.2 Gradients

| Name | Value | Usage |
|------|-------|-------|
| `--grad-brand` | `linear-gradient(to right, #9333EA, #EC4899)` | Primary CTAs, hero text, brand moments |
| `--grad-cool` | `linear-gradient(to right, #6366F1, #06B6D4)` | Secondary elements, info cards |
| `--grad-holo` | `linear-gradient(135deg, #00E5FF, #E144FF, #A7B4C6)` | Psychat-specific elements |
| `--grad-subtle` | `radial-gradient(circle at 30% 30%, rgba(147,51,234,0.15), transparent 50%)` | Background ambiance |

### 4.3 Typography

#### Font Stack (3 fonts max + 1 product-specific)

| Role | Font | Weight | Usage |
|------|------|--------|-------|
| **Body** | Inter | 400, 500, 600 | All body text, UI labels, buttons |
| **Headings** | Jura | 500, 600, 700 | Section headings, hero text, navigation |
| **Code/Terminal** | JetBrains Mono | 400, 500 | Wallet addresses, code, Psychat terminal |
| **Display** (Psychat only) | Orbitron | 600, 700 | Psychat hero headlines, special displays |

**Dropped:** Playfair Display (doesn't fit Web3 aesthetic), Share Tech Mono (redundant with JetBrains Mono).

#### Type Scale

| Level | Size | Line Height | Weight | Font |
|-------|------|-------------|--------|------|
| Display | clamp(2.5rem, 5vw, 4rem) | 1.1 | 700 | Jura |
| H1 | clamp(2rem, 4vw, 3rem) | 1.15 | 700 | Jura |
| H2 | clamp(1.5rem, 3vw, 2.25rem) | 1.2 | 600 | Jura |
| H3 | clamp(1.25rem, 2.5vw, 1.75rem) | 1.3 | 600 | Jura |
| H4 | 1.125rem | 1.4 | 600 | Jura |
| Body Large | 1.125rem | 1.6 | 400 | Inter |
| Body | 1rem (16px) | 1.6 | 400 | Inter |
| Body Small | 0.875rem | 1.5 | 400 | Inter |
| Caption | 0.75rem | 1.4 | 500 | Inter |
| Code | 0.875rem | 1.5 | 400 | JetBrains Mono |

**Minimum body text: 16px.** No exceptions on any product.

### 4.4 Spacing Scale

Based on 4px grid:

| Token | Value |
|-------|-------|
| `--space-1` | 4px |
| `--space-2` | 8px |
| `--space-3` | 12px |
| `--space-4` | 16px |
| `--space-6` | 24px |
| `--space-8` | 32px |
| `--space-12` | 48px |
| `--space-16` | 64px |
| `--space-24` | 96px |

### 4.5 Grid

- **Max content width:** 1280px (site), 1440px (app)
- **Columns:** 12-column grid
- **Gutter:** 24px (desktop), 16px (mobile)
- **Margin:** 48px (desktop), 16px (mobile)

### 4.6 Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | 8px | Small buttons, badges |
| `--radius-md` | 12px | Cards, inputs |
| `--radius-lg` | 16px | Panels, modals |
| `--radius-xl` | 24px | Hero cards, glass panels |
| `--radius-full` | 9999px | Pills, avatars |
| `--radius-none` | 0 | Psychat Matrix/terminal elements only |

### 4.7 Iconography

- **Style:** Outlined, 1.5px stroke, rounded caps
- **Library:** Lucide Icons (primary), custom for brand-specific concepts
- **Size:** 20px (default), 16px (compact), 24px (emphasis)
- **Color:** Inherit from text color or use brand gradient for emphasis

### 4.8 Motion Style

| Pattern | Duration | Easing | Usage |
|---------|----------|--------|-------|
| Micro-interaction | 150ms | `cubic-bezier(0.4, 0, 0.2, 1)` | Button press, toggle |
| Transition | 300ms | `cubic-bezier(0.4, 0, 0.2, 1)` | Page transitions, card hover |
| Entrance | 500ms | `cubic-bezier(0, 0, 0.2, 1)` | Element fade-in, slide-up |
| Ambient | 6-8s | `ease-in-out` | Background gradients, floating elements |

**Psychat exceptions:** May use neon-flicker (sparingly), holographic-scan (background only), edge-glow-pulse (interactive elements). These MUST NOT appear on Hub or main site.

**Reduced motion:** All animations must respect `prefers-reduced-motion: reduce`. Replace motion with instant state changes.

---

## 5. Logo Usage

### Primary Mark
**The pastel gradient app icon** (rounded square with lambda/human figure) is the primary logomark. Reference: `10.png`, `11.png`, `MotusDAO logop.png`.

**Rationale:** It's modern, versatile, works at small sizes, and communicates both tech and humanity. The badge/coin logo (`logo iconmotus.svg`) is too complex for small sizes and too crypto-centric.

### Logo Variants

| Variant | Use Case |
|---------|----------|
| **Logomark** (icon only) | Favicons, app icons, social avatars, compact spaces |
| **Logotype** (icon + "MotusDAO") | Navigation bars, headers, formal contexts |
| **Wordmark** ("MotusDAO" text only) | When icon is already present nearby |

### Minimum Sizes
- **Logomark:** 24px (digital), 10mm (print)
- **Logotype:** 120px wide (digital), 30mm (print)

### Clear Space
Minimum clear space around the logo = height of the "M" in MotusDAO on all sides. No other elements may enter this zone.

### Allowed Backgrounds
- ✅ Solid dark (`#000000`, `#0B101A`)
- ✅ Solid white (`#FFFFFF`) — use dark version of logotype
- ✅ Brand gradient background (with sufficient contrast)
- ✅ Glass/blur panels (with padding)

### Prohibited Treatments
- ❌ Stretching or distorting the logo
- ❌ Rotating the logo
- ❌ Adding drop shadows, outlines, or effects not in the original
- ❌ Placing on busy photo backgrounds without a semi-opaque overlay
- ❌ Changing the gradient colors of the logomark
- ❌ Using the old badge/coin logo (`logo iconmotus.svg`) as primary — it may appear in legacy contexts but should not be used in new materials
- ❌ Recreating the logo in different fonts

---

## 6. Component Rules

### 6.1 Hero Section

```
┌──────────────────────────────────────┐
│ [subtle gradient bg / glass overlay] │
│                                      │
│   H1: Jura 700, gradient text        │
│   max-width: 720px, centered         │
│                                      │
│   Subhead: Inter 400, text-secondary │
│   max-width: 560px                   │
│                                      │
│   [CTA Button] [Secondary Button]    │
│                                      │
│   Trust signal: "X users · Y chain"  │
│                                      │
└──────────────────────────────────────┘
```

- Background: dark with `--grad-subtle` radials
- CTA: Primary gradient button, min 48px height
- No stock photos. Use abstract graphics, screenshots, or nothing.
- Max 2 CTAs. Primary + ghost/secondary.

### 6.2 Cards

**Standard Card:**
- Background: `--bg-surface` with `backdrop-blur: 20px`
- Border: `1px solid var(--border-default)`
- Radius: `--radius-lg`
- Padding: `--space-6`
- Hover: `translateY(-2px)`, `shadow-glow`

**Proof Card** (for metrics/social proof):
- Same base as standard card
- Metric: Jura 700, gradient text, large
- Label: Inter 400, text-secondary, small
- Optional: subtle animated background gradient

### 6.3 CTA Blocks

```
┌─────────────────────────────────┐
│  Glass panel, centered content  │
│                                 │
│  H3: Action-oriented heading    │
│  Body: One line of context      │
│                                 │
│  [Primary CTA Button]           │
│                                 │
└─────────────────────────────────┘
```

- Always full-width within container
- Must have clear value proposition (not just "Learn More")
- Button text: verb + noun ("Start a session", "Connect wallet", "View payments")

### 6.4 Proof Blocks (Social Proof / Metrics)

```
┌───────┐  ┌───────┐  ┌───────┐
│ 1,200 │  │  <10s │  │  $0   │
│ users │  │ txn   │  │ fees  │
└───────┘  └───────┘  └───────┘
```

- Grid: 3-4 columns on desktop, 2 on mobile
- Number: Display size, gradient text
- Label: Caption size, text-secondary
- Use verifiable metrics only

### 6.5 Thread Visuals (X/Twitter)

- Format: 1:1 or 4:5 image cards
- Background: solid `#000000` or `--bg-secondary`
- Content: large text (Jura 700) + supporting visual
- Brand mark: bottom-right corner, small logomark
- Border: 1px `--border-default` or gradient border
- No stock photos. Screenshots, diagrams, or text-only.

---

## 7. Accessibility

### Contrast Requirements (WCAG AA)
- Body text on backgrounds: minimum **4.5:1**
- Large text (≥18px bold or ≥24px): minimum **3:1**
- Interactive elements: minimum **3:1**
- Focus indicators: visible, **3:1** against adjacent colors

### Known Risk Areas
| Combination | Ratio | Status | Fix |
|-------------|-------|--------|-----|
| `--text-primary` on `--bg-primary` | ~17:1 | ✅ Pass | — |
| `--text-secondary` on `--bg-primary` | ~8.5:1 | ✅ Pass | — |
| `--brand-cyan` on `--bg-secondary` | ~8.2:1 | ✅ Pass | — |
| `--brand-purple` on `--bg-primary` | ~3.8:1 | ⚠️ AA Large only | Use for headings, not body |
| Neon cyan text-shadow on dark | Variable | ⚠️ Test | Ensure base text passes without shadow |

### Minimum Sizes
- Body text: 16px
- Button text: 14px
- Touch targets: 44x44px minimum
- Logo: 24px minimum

### Reduced Motion
All products must implement:
```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

### Screen Reader Considerations
- All images must have descriptive `alt` text
- Interactive elements must have accessible labels
- Page structure must use semantic HTML (`<nav>`, `<main>`, `<section>`, `<h1>`-`<h6>`)
- Gradient text must have a fallback solid color for forced-colors mode

---

## 8. Do / Don't

### Visual Do's ✅
- Use dark backgrounds as default
- Apply glassmorphism with `backdrop-blur` for elevation
- Use gradient text for hero headings and key metrics
- Keep imagery abstract or use real screenshots
- Use the unified spacing scale
- Apply the brand gradient to primary CTAs

### Visual Don'ts ❌
- Don't use white/light backgrounds as primary (Hub, Psychat) — main site can use light bg only if re-skinned with brand tokens
- Don't use stock photos of people looking happy/sad
- Don't use more than 2 gradients per viewport
- Don't mix rounded and sharp corners in the same product (except Psychat terminal elements)
- Don't use orange, coral, or warm accents (legacy color — remove from main site)
- Don't use Playfair Display or Share Tech Mono in any new work

### Verbal Do's ✅
- Lead with what's built, not what's planned
- Use precise technical language ("E2E encrypted on Solana" not "secure")
- Quantify claims ("1,200 users" not "thousands")
- Acknowledge limitations honestly
- Use active voice

### Verbal Don'ts ❌
- Don't say "revolutionizing" or "disrupting"
- Don't use savior language ("saving mental health", "helping the helpless")
- Don't make medical claims
- Don't promise token returns or financial outcomes
- Don't use "Web3" without substance behind it
- Don't say "decentralized" about centralized components
- Don't use "innovative" or "cutting-edge" as standalone claims

---

## 9. Brand QA Checklist

Run this checklist before publishing ANY new design or copy asset.

### Visual Checklist
- [ ] Uses correct logo variant (primary mark, not legacy badge)
- [ ] Logo has minimum clear space
- [ ] Colors match unified palette tokens (no hardcoded hex outside system)
- [ ] Typography uses only approved fonts (Inter, Jura, JetBrains Mono, Orbitron for Psychat)
- [ ] Body text ≥ 16px
- [ ] All color combinations meet WCAG AA contrast
- [ ] Touch/click targets ≥ 44px
- [ ] Spacing follows 4px grid
- [ ] No stock photos
- [ ] Gradients used ≤ 2 per viewport
- [ ] Reduced motion support verified
- [ ] Dark mode is default (or appropriate for product)

### Copy Checklist
- [ ] No prohibited claims (see Section 3)
- [ ] No savior tone
- [ ] Active voice throughout
- [ ] Specific and verifiable where making claims
- [ ] Appropriate tone for the channel (see Section 2)
- [ ] No medical claims or therapy guarantees
- [ ] CTA text is verb + noun
- [ ] Maximum 2 CTAs visible at once

### Pre-Publish
- [ ] Reviewed by at least one team member
- [ ] Matches a defined template (see doc 04)
- [ ] Cross-product links use correct URLs
- [ ] Tested on mobile viewport
- [ ] Social preview (og:image, og:title) set correctly
