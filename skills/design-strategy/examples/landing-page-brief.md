# Design Strategy: Product Landing Page

*Compact example showing Discovery → Specification for a landing page*

---

## Discovery

### Target User

**Persona: Alex — Technical Founder**

**Role:** Solo founder building a developer tool
**Tech comfort:** High
**Goal:** Evaluate whether this product solves their problem in under 60 seconds
**Frustration:** Landing pages that hide pricing, bury the demo, or use vague marketing language
**Context:** Found this via a Hacker News comment or Twitter link. Has 15 tabs open. Will bounce in 10 seconds if the value prop isn't clear.

### Jobs-to-Be-Done

```
When I click a link to a new developer tool,
I want to immediately understand what it does and see it working,
so I can decide whether to try it or close the tab.
```

```
When I'm comparing three similar tools,
I want to see pricing and limitations upfront,
so I can shortlist without signing up for each one.
```

### Competitive Patterns

What developer landing pages do well:
- **Linear:** Clean, fast, feature sections with inline demos
- **Vercel:** Strong hero, clear CTA, social proof from recognizable logos
- **Raycast:** Interactive demo embedded in the page

What they do poorly:
- Feature overload — 15 sections nobody scrolls to
- "Book a demo" as the only CTA (technical founders want self-serve)
- Hiding pricing behind "Contact Sales"

---

## Architecture: Page Sections

```markdown
1. **Hero** — One-sentence value prop + primary CTA + visual/demo
2. **Problem** — 2-3 pain points the audience recognizes ("You know this feeling...")
3. **Solution** — How the product works in 3 steps or a short demo
4. **Social proof** — Logos, testimonials, or usage numbers
5. **Features** — 3-4 key capabilities with brief descriptions
6. **Pricing** — Clear tiers, visible on the page (not hidden)
7. **FAQ** — 4-6 common objections answered
8. **Final CTA** — Repeat the primary action
```

### Content Hierarchy: Hero Section

**Primary:**
- Headline: One sentence that describes what the product does (not a tagline)
- Primary CTA button: "Try it free" or "Get started"

**Secondary:**
- Sub-headline: One sentence on how it works or who it's for
- Visual: Product screenshot, short video, or interactive demo

**Tertiary:**
- Secondary CTA: "View docs" or "See pricing"
- Social proof line: "Used by 2,000+ developers" or logo strip

---

## Specification: Design Brief

**Overview:** Landing page for a developer tool targeting technical founders and senior engineers. Must communicate value in under 10 seconds and provide a self-serve path to trying the product.

**Design Principles:**
1. **Clarity over cleverness** — Say what it does, not what it metaphorically represents
2. **Show, don't tell** — Inline demos and code samples over feature descriptions
3. **Respect the visitor's time** — No fluff sections, no "book a demo" gates

**Success Metrics:**
- Time to understand value prop: < 10 seconds
- Scroll depth: 60%+ reach the pricing section
- CTA click rate: > 5% on primary CTA

**Accessibility:**
- All text meets 4.5:1 contrast on chosen background
- CTA buttons are at least 44x44px touch targets
- Demo/video has keyboard controls and captions
- Page is navigable via keyboard (skip to content, logical focus order)

**Technical Constraints:**
- Must load in < 2 seconds on 3G (no heavy frameworks for a landing page)
- Works without JavaScript (content visible, interactive elements progressively enhanced)
- Responsive: mobile-first, breakpoints at 640px, 1024px, 1280px

---

*Hand off to `frontend-design` with: "Build this landing page following the design brief above. Hero section first, then remaining sections. Use the content hierarchy for visual weight decisions."*
