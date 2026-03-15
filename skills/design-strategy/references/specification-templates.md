# Specification Templates

## Design Brief

A one-page summary of the project that aligns stakeholders and guides implementation.

```markdown
# Design Brief: [Project Name]

## Overview
[2-3 sentences: what is this product/feature, who is it for, and why does it matter?]

## Problem Statement
[JTBD format: When [situation], I want to [action], so I can [outcome].]

## Target Users
| Persona | Primary Goal | Key Constraint |
|---------|-------------|----------------|
| [Name]  | [Goal]      | [Constraint]   |
| [Name]  | [Goal]      | [Constraint]   |

## Success Metrics
- [Metric 1: e.g., "New user completes onboarding in < 3 minutes"]
- [Metric 2: e.g., "Support tickets for billing reduced by 40%"]
- [Metric 3]

## Scope
**In scope:**
- [Feature/capability]
- [Feature/capability]

**Out of scope:**
- [Feature/capability] — [Why deferred]

## Design Principles
1. **[Principle]** — [One-sentence explanation]
2. **[Principle]** — [One-sentence explanation]
3. **[Principle]** — [One-sentence explanation]

## Technical Constraints
- [Framework, platform, browser support requirements]
- [Performance targets]
- [Accessibility requirements — WCAG 2.2 AA minimum]

## Timeline
| Milestone | Date | Deliverable |
|-----------|------|-------------|
| [Phase]   | [Date] | [What's delivered] |

## Open Questions
- [ ] [Question that needs answering before implementation]
- [ ] [Question that needs stakeholder input]
```

## Component Specification

Detailed spec for a UI component — enough for a developer to build it without guessing.

```markdown
## Component: [Component Name]

### Purpose
[One sentence: what does this component do and where does it appear?]

### Anatomy
- [Element 1: e.g., "Header — contains title and action buttons"]
- [Element 2: e.g., "Body — scrollable content area"]
- [Element 3: e.g., "Footer — contains primary and secondary actions"]

### Props / Configuration
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| [name] | [type] | [default] | [what it controls] |

### States
| State | Appearance | Behavior |
|-------|-----------|----------|
| Default | [Description] | [Interactions available] |
| Hover | [What changes] | [What happens] |
| Active/Pressed | [What changes] | [Feedback shown] |
| Disabled | [Visual treatment] | [No interactions, tooltip explains why] |
| Loading | [Skeleton/spinner] | [Non-interactive] |
| Error | [Error styling] | [How to recover] |

### Interactions
- **Click/Tap:** [What happens]
- **Keyboard:** [Tab order, Enter/Space behavior, Escape behavior]
- **Screen reader:** [ARIA role, label, live region announcements]

### Responsive Behavior
| Breakpoint | Behavior |
|-----------|----------|
| Desktop (>1024px) | [Layout description] |
| Tablet (768-1024px) | [What changes] |
| Mobile (<768px) | [What changes] |

### Content Guidelines
- [Character limits, truncation rules]
- [Tone/voice for labels and messages]
- [Placeholder text guidelines]
```

## WCAG 2.2 AA Accessibility Checklist

Run through this checklist for every design. Items marked with * are commonly missed.

### Perceivable
- [ ] Color contrast: 4.5:1 for normal text, 3:1 for large text (18px+ or 14px+ bold)
- [ ] * Non-text contrast: 3:1 for UI components and meaningful graphics
- [ ] Information is not conveyed by color alone (add icons, patterns, or labels)
- [ ] * All images have meaningful alt text (or empty alt="" for decorative images)
- [ ] Video has captions; audio has transcripts
- [ ] * Content is readable and functional at 200% zoom
- [ ] * Text spacing can be adjusted without loss of content (1.5x line height, 2x paragraph spacing)

### Operable
- [ ] All interactive elements are keyboard accessible (Tab, Enter, Space, Escape, Arrow keys)
- [ ] * Focus order is logical and visible (no focus traps except modals)
- [ ] * Focus indicator is clearly visible (not just browser default)
- [ ] No content flashes more than 3 times per second
- [ ] Skip navigation link for keyboard users
- [ ] * Touch targets are at least 24x24px (44x44px recommended for mobile)
- [ ] * Hover/focus content (tooltips, dropdowns) is dismissible, hoverable, and persistent

### Understandable
- [ ] Page language is declared (`lang` attribute)
- [ ] * Form inputs have visible labels (not just placeholders)
- [ ] * Error messages identify the field and describe how to fix the error
- [ ] * Required fields are indicated before submission, not just after
- [ ] Navigation is consistent across pages

### Robust
- [ ] Valid HTML with proper semantic elements
- [ ] * ARIA roles and properties are used correctly (or not at all — semantic HTML first)
- [ ] * Dynamic content changes are announced to screen readers (aria-live regions)
- [ ] * Custom components follow WAI-ARIA authoring practices

## Developer Handoff Document

```markdown
# Handoff: [Feature/Component Name]

## Context
[Link to design brief, user flows, and any relevant discovery artifacts]

## Implementation Priority
1. [First thing to build — usually the happy path]
2. [Second priority — core interactions]
3. [Third — error handling and edge cases]
4. [Last — polish, animations, empty states]

## Key Decisions
- [Decision 1: e.g., "Pagination over infinite scroll — dataset can be 100k+ rows"]
- [Decision 2: e.g., "Client-side filtering — most users have < 500 items"]

## Data Requirements
| Field | Type | Source | Notes |
|-------|------|--------|-------|
| [field] | [type] | [API endpoint or state] | [any caveats] |

## States to Implement
[Reference the state map from IA phase — list all states this component/feature needs]

## Accessibility Requirements
[Key accessibility items from the checklist — focus on non-obvious ones]

## Open Questions for Engineering
- [ ] [Question about feasibility or approach]
- [ ] [Question about data availability]
```
