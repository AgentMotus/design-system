# 05 — Plan de Implementación 30 Días / 30-Day Implementation Plan

**Start Date:** 2026-03-01  
**Owner:** MotusDAO design/dev team

---

## Week 1 (Days 1–7) — P1: Foundation

### Day 1–2: Token Unification
- [ ] Create shared `tokens.css` file from doc 04
- [ ] Create shared `tailwind.config.js` preset from doc 04
- [ ] Add unified font import to Hub and Psychat
- [ ] **Owner:** Lead developer
- [ ] **Deliverable:** PR with shared tokens package/file

### Day 3–4: Logo Standardization
- [ ] Export primary logomark (pastel gradient icon) as SVG, PNG @1x/2x/3x
- [ ] Create dark-background and light-background logotype variants
- [ ] Replace all logo instances in Hub with primary mark
- [ ] Replace favicon across all 3 products
- [ ] **Owner:** Designer + lead developer
- [ ] **Deliverable:** `/assets/logos/` directory with all variants

### Day 5–7: Hub Token Migration
- [ ] Replace hardcoded colors in Hub with unified tokens
- [ ] Drop Playfair Display and Share Tech Mono from Hub font imports
- [ ] Verify no visual regressions (screenshot diff)
- [ ] **Owner:** Hub developer
- [ ] **Deliverable:** Hub running on unified tokens, PR merged

**Week 1 Exit Criteria:** Hub uses unified tokens. Logo is standardized. Shared config exists.

---

## Week 2 (Days 8–14) — P1: Main Site Triage + Psychat Alignment

### Day 8–10: Main Site Critical Fixes
- [ ] Replace all logo instances with primary mark
- [ ] Fix hero CTA: increase contrast, rewrite copy (verb + noun)
- [ ] Increase body text to minimum 16px
- [ ] Remove orange/coral colors — replace with brand purple accents
- [ ] Fix footer alignment
- [ ] Add shared navigation style (dark bg, brand colors)
- [ ] **Owner:** Main site developer (Wix constraints may limit some changes)
- [ ] **Deliverable:** Main site with improved visual alignment

### Day 11–12: Psychat Token Alignment
- [ ] Import unified tokens, map Psychat overrides on top
- [ ] Ensure shared navigation/footer matches ecosystem style
- [ ] Switch body text from JetBrains Mono to Inter (keep mono for terminal elements)
- [ ] Verify holographic animations still work with new token names
- [ ] **Owner:** Psychat developer
- [ ] **Deliverable:** Psychat running on unified tokens

### Day 13–14: Cross-Product Navigation
- [ ] Implement shared footer across all 3 products (same links, same layout)
- [ ] Add ecosystem links in each product's navigation (Hub ↔ Psychat ↔ Main)
- [ ] Ensure consistent favicon and og:image across all products
- [ ] **Owner:** All developers
- [ ] **Deliverable:** User can navigate between products with visual continuity

**Week 2 Exit Criteria:** All 3 products share tokens. Cross-navigation exists. Main site critical issues fixed.

---

## Week 3 (Days 15–21) — P2: Templates + Content

### Day 15–16: Social Templates
- [ ] Create X post template (1:1) in Figma or Canva using unified tokens
- [ ] Create X vertical template (9:16)
- [ ] Create partnership announcement template
- [ ] **Owner:** Designer
- [ ] **Deliverable:** 3 reusable templates in team design tool

### Day 17–18: Proof System
- [ ] Implement proof card component in Hub (reusable)
- [ ] Add metrics section to main site hero (users, sessions, chains)
- [ ] Verify all displayed metrics are accurate and sourced
- [ ] **Owner:** Hub developer + content lead
- [ ] **Deliverable:** Proof cards live on Hub and main site

### Day 19–21: Content Audit + Rewrite
- [ ] Audit all copy on main site against Messaging System (doc 03, section 3)
- [ ] Remove prohibited claims
- [ ] Rewrite hero copy: lead with sovereignty/infrastructure message
- [ ] Rewrite course card copy: tighten, improve hierarchy
- [ ] **Owner:** Content lead / copywriter
- [ ] **Deliverable:** Updated copy across main site

**Week 3 Exit Criteria:** Social templates ready. Proof system live. Copy aligned with brand voice.

---

## Week 4 (Days 22–30) — P2/P3: Polish + Process

### Day 22–24: Accessibility Pass
- [ ] Run contrast checks on all 3 products (use axe-core or similar)
- [ ] Fix any WCAG AA failures
- [ ] Verify reduced motion implementation
- [ ] Test all products on mobile viewports
- [ ] **Owner:** All developers
- [ ] **Deliverable:** Accessibility report, all AA issues resolved

### Day 25–27: Banner + OG Image Refresh
- [ ] Create new banner set using unified system (1500×500, 1200×675, 1080×1080)
- [ ] Update X/Twitter, Telegram, and all social profile images
- [ ] Set og:image on all pages across all products
- [ ] **Owner:** Designer
- [ ] **Deliverable:** Consistent social presence

### Day 28–29: Brand Guardian Setup
- [ ] Share Brand Guardian prompt (doc 06) with all team members
- [ ] Add Brand QA Checklist (doc 03, section 9) to PR template
- [ ] Document token file locations in repo README
- [ ] **Owner:** Lead developer + content lead
- [ ] **Deliverable:** Process integrated into workflow

### Day 30: Review + Next Phase Planning
- [ ] Full visual walkthrough: main site → Hub → Psychat
- [ ] Screenshot all 3 products, compare to Day 1 screenshots
- [ ] Document remaining issues for v1.1
- [ ] Decide: migrate main site off Wix? (P3 — next quarter)
- [ ] **Owner:** Team
- [ ] **Deliverable:** v1 implementation complete, v1.1 roadmap drafted

---

## Priority Summary

| Priority | Items | Timeline |
|----------|-------|----------|
| **P1** | Token unification, logo standardization, Hub migration, main site critical fixes, Psychat alignment, cross-nav | Week 1–2 |
| **P2** | Social templates, proof system, content rewrite, accessibility, banner refresh, Brand Guardian process | Week 3–4 |
| **P3** | Main site migration off Wix, advanced component library, motion system refinement, Figma design system | Next quarter |

---

## Success Metrics (Day 30)

- [ ] All 3 products use the same color tokens
- [ ] One logo appears across all touchpoints
- [ ] Body text ≥ 16px everywhere
- [ ] No orange/coral colors anywhere
- [ ] Cross-product navigation exists
- [ ] At least 3 social templates in use
- [ ] Brand QA Checklist integrated into workflow
- [ ] WCAG AA compliance on all 3 products
