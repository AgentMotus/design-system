# 01 — Auditoría Comparativa / Comparative Audit

**Date:** 2026-02-27  
**Scope:** motusdao.org (Main Site) · app.motusdao.org (Hub) · psychat.motusdao.org (Psychat)

---

## Executive Summary

The three MotusDAO products feel like three separate brands. The Hub is the most mature and coherent. The main site (Wix) is visually fragmented and undermines credibility. Psychat is aesthetically strong but completely disconnected from the rest of the ecosystem. Unifying them under a single brand system is the #1 priority.

---

## 🔴 Critical Findings

### C1 — Three different visual identities
- **Main site:** White backgrounds, purple accents, serif hero headings, Wix stock patterns, warm orange-coral gradients
- **Hub:** Dark-first glassmorphism, purple-pink gradient system, Inter/Jura typography, polished
- **Psychat:** Holographic terminal aesthetic, cyan/magenta palette, JetBrains Mono, zero overlap with the other two

**Impact:** A user visiting motusdao.org → app.motusdao.org → psychat.motusdao.org has no visual thread connecting the three. This destroys brand trust and suggests three unrelated projects.

**Fix:** Implement unified color tokens, shared typography stack, and a consistent dark-mode-first base across all three. See Manual v1 (doc 03).

### C2 — Main site (Wix) looks generic and underbaked
- Course cards are text-heavy, cramped, inconsistent layouts
- Blog thumbnails introduce random colors with no brand filter
- Hero CTA ("Visita nuestro curso más comprado") has poor contrast and weak copy
- Typography mixes decorative serif hero with utilitarian sans elsewhere — split personality
- Footer layout is misaligned
- The site looks like a template, not a branded product

**Impact:** First-touch credibility. Most visitors will arrive here first. It signals "side project" not "hyperstructure."

**Fix:** Redesign or heavily re-skin the Wix site using the unified design system. If Wix constrains execution, migrate to a static site (Next.js / Astro) matching Hub's aesthetic.

### C3 — Logo inconsistency across assets
- `logo iconmotus.svg`: Circular badge/coin with magenta wireframe, dark bg — Web3 crypto aesthetic
- `MotusDAO logop.png` / `10.png` / `11.png`: Soft pastel gradient rounded square with white lambda-like figure — wellness/app aesthetic
- Banner variants: Dark bg with 3D chrome blobs, neon accents

**Impact:** There are effectively 2-3 different logos in circulation. No clear primary mark.

**Fix:** Designate ONE primary logomark and ONE wordmark. Define usage rules (doc 03, Logo Usage section).

### C4 — No shared color system
| Token | Main Site | Hub | Psychat |
|-------|-----------|-----|---------|
| Primary | ~#6B2FD6 (purple) | #9333ea → #ec4899 (gradient) | #00E5FF (cyan) |
| Background | White | #000000 | #0B101A |
| Accent | Orange-coral | #6366f1 (blue) | #E144FF (magenta) |
| Typography | Mixed serif + sans | Inter / Jura | JetBrains Mono / Orbitron |

**Fix:** Define a single palette with product-specific accent allowances (doc 04).

---

## 🟡 Medium Findings

### M1 — Typography stack is too wide
Across the ecosystem: Inter, Jura, Playfair Display, Share Tech Mono, Orbitron, JetBrains Mono, plus Wix's default fonts. That's 7+ typefaces.

**Fix:** Consolidate to 3 max: Inter (body), Jura (headings), JetBrains Mono (terminal/code). Drop Playfair Display, Share Tech Mono. Keep Orbitron only for Psychat display headings.

### M2 — Accessibility gaps
- Main site: Small body text, low-contrast CTAs, text over gradients without sufficient overlay
- Hub payments page: Yellow/amber icons disconnected from palette, status badges lack systematic color mapping
- Psychat: Neon text on dark backgrounds — potential WCAG issues with cyan on near-black

**Fix:** Enforce WCAG AA minimum (4.5:1 body, 3:1 large text). Add contrast checking to Brand QA Checklist.

### M3 — Motion inconsistency
- Hub: Subtle lifts and scales, well-tuned cubic-bezier
- Psychat: Heavy animations (holographic scans, neon flicker, floating panels)
- Main site: Wix default transitions

**Fix:** Define a shared motion language. Psychat can be more expressive but within bounds.

### M4 — Banner assets are inconsistent
- `banner motusdao.png`: Clean but old aesthetic
- `banner motusdao new.png`: 3D chrome blobs, neon — modern but doesn't match main site
- Social banner variants: Different styles within the same batch

**Fix:** Create 1 banner template system with locked elements (logo position, tagline placement, background treatment).

---

## 🟢 Minor Findings / What's Working

### W1 — Hub design system is solid
The `DESIGN_SYSTEM-HUB.md` is comprehensive: proper tokens, theme variants, component patterns, accessibility notes, glassmorphism system. This is the foundation to build on.

### W2 — Psychat design system is creative and consistent within itself
The holographic terminal aesthetic is well-executed and unique. The problem is isolation, not quality.

### W3 — Brand narrative is strong
"AI-Human Hybrid Mental Healthcare" — clear, differentiated, not generic. The execution-first thesis (hyperstructure, self-custody, dataconomy) is compelling when communicated well.

### W4 — Dark-mode-first works for the category
Both Hub and Psychat default to dark. This aligns with Web3 audiences and differentiates from clinical-white health platforms.

### W5 — Logo concept (pastel gradient variant) has potential
The rounded-square app icon with the lambda/human figure is modern and versatile. Could work as the primary mark with refinement.

---

## Priority Matrix

| Finding | Severity | Effort | Impact | Priority |
|---------|----------|--------|--------|----------|
| C1 — Three identities | Critical | High | Highest | P1 |
| C2 — Main site quality | Critical | High | High | P1 |
| C3 — Logo inconsistency | Critical | Medium | High | P1 |
| C4 — No shared colors | Critical | Medium | High | P1 |
| M1 — Typography bloat | Medium | Low | Medium | P2 |
| M2 — Accessibility gaps | Medium | Medium | High | P2 |
| M3 — Motion inconsistency | Medium | Low | Low | P3 |
| M4 — Banner inconsistency | Medium | Low | Medium | P2 |

---

## Missing Assets (Needed for Full Audit)

1. **Psychat expanded screenshot** — file too large to analyze (24MB), needs compression
2. **Course page screenshot** — not analyzed, likely similar issues to academia page
3. **SVG logo** — couldn't render; need PNG export of the badge logo for comparison
4. **Brand guidelines from Wix** — any existing font/color settings in the Wix editor
5. **Analytics data** — which product gets most traffic? This affects redesign priority
6. **Competitive screenshots** — for benchmarking against similar platforms (Calm, BetterHelp, Ethereum-native health projects)
