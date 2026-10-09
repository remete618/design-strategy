# design-strategy

**The thinking before the pixels.**

A Claude Code skill for strategic design thinking — user research, discovery, user flows, information architecture, specifications, and design critique. Every other design skill helps you build prettier UI. This one helps you figure out *what to build*.

## Install

Register this repo as a plugin marketplace once, then install the plugin from it:

```bash
claude plugin marketplace add remete618/design-strategy
claude plugin install design-strategy@design-strategy
```

To try it without installing, point Claude Code at a local clone:

```bash
git clone https://github.com/remete618/design-strategy.git
claude --plugin-dir ./design-strategy
```

## What it does

design-strategy guides Claude through a 5-phase **Design Strategy Loop**, producing concrete markdown artifacts at each step:

| Phase | What you get |
|-------|-------------|
| **Discovery** | User personas, JTBD problem statements, competitive analysis |
| **Definition** | User flow diagrams (Mermaid), journey maps, feature prioritization (MoSCoW/RICE) |
| **Architecture** | Site maps, navigation models, content hierarchy, state mapping |
| **Specification** | Design briefs, component specs, WCAG 2.2 AA checklist, dev handoff docs |
| **Critique** | Heuristic evaluation scorecard, accessibility audit, consistency report |

## Example prompts

```
Plan the UX for a SaaS analytics dashboard
```

```
Create user personas for an e-commerce app targeting small business owners
```

```
Map the checkout user flow for a subscription product
```

```
Audit this landing page design for usability issues
```

```
Write a design brief for a mobile onboarding flow
```

```
Prioritize these features for our MVP: [list of features]
```

## How it works with other skills

design-strategy is designed to complement implementation skills:

1. **Run design-strategy** to figure out what to build and why
2. **Hand off to frontend-design** (or similar) to build it

The artifacts produced here — design briefs, component specs, user flows — become the input for implementation. Better strategy = better implementation.

## What's inside

```
skills/design-strategy/
├── SKILL.md                          # Core 5-phase process
├── references/
│   ├── discovery-frameworks.md       # Personas, JTBD, competitive analysis
│   ├── definition-templates.md       # User flows, journey maps, prioritization
│   ├── ia-patterns.md                # Navigation, content hierarchy, state mapping
│   ├── specification-templates.md    # Design briefs, component specs, WCAG, handoff
│   └── critique-frameworks.md        # Nielsen's heuristics, accessibility audit
└── examples/
    ├── saas-dashboard-strategy.md    # Full 5-phase worked example
    └── landing-page-brief.md         # Compact discovery → spec example
```

References are loaded progressively — only when the relevant phase is active — to keep context usage low.

## Output format

All artifacts are **markdown** with:
- Mermaid diagrams for flows and architectures
- Tables for matrices and comparisons
- Checklists for audits and specifications

Everything renders in GitHub, Obsidian, Notion, and most documentation tools.

## License

MIT
