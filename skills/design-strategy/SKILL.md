---
name: design-strategy
description: Strategic design thinking — user research, discovery, user flows, information architecture, design specifications, and design critique. Use this skill when the user asks to plan a product's UX, create user personas, map user flows or journeys, audit or critique a design, build an information architecture, write a design brief, prioritize features, or do any upstream design work before implementation. This skill is about figuring out WHAT to build and WHY — use it before reaching for implementation skills like frontend-design. Trigger on phrases like "plan the UX", "user flow", "design strategy", "user personas", "IA", "information architecture", "design audit", "design critique", "journey map", "feature prioritization", "design brief", "component spec", "accessibility audit", or any request that needs design thinking before code.
---

# Design Strategy

The thinking before the pixels. This skill produces structured design artifacts — personas, flows, architectures, specs, and critiques — that make implementation faster and more intentional.

## When to use this skill

Use design-strategy when the work is about **what to build and why**, not how to code it. Typical triggers:

- "Plan the UX for..." / "Design the user experience of..."
- "Create user personas for..." / "Who are the users of...?"
- "Map the user flow for..." / "What's the checkout flow?"
- "Audit this design" / "Critique this landing page"
- "Write a design brief for..." / "Spec out this feature"
- "Prioritize these features" / "What should we build first?"
- "What's the information architecture for...?"
- "Create a journey map for..."

After design-strategy produces artifacts, hand off to `frontend-design` or similar skills for implementation.

## The Design Strategy Loop

Work through these phases in order. Each phase produces a **concrete markdown artifact**, not just advice. Skip phases the user doesn't need — but when in doubt, start from Discovery.

### Phase 1: Discovery

Understand the problem space before proposing solutions.

**Artifacts produced:**
- User personas (2-4, with goals, frustrations, and context)
- Problem statements using Jobs-to-Be-Done format
- Competitive analysis matrix

Load `references/discovery-frameworks.md` for persona templates, JTBD syntax, and competitive analysis structure.

**Process:**
1. Ask clarifying questions about the product, audience, and business goals
2. Draft personas based on what's known — mark assumptions explicitly
3. Frame the core problem as JTBD statements
4. If competitors are mentioned, build a comparison matrix

### Phase 2: Definition

Translate discovery into structure.

**Artifacts produced:**
- User flow diagrams (Mermaid syntax — renders in GitHub, Obsidian, most markdown tools)
- Journey maps with emotional states and pain points
- Feature prioritization matrix (MoSCoW or RICE)

Load `references/definition-templates.md` for flow diagram patterns, journey map format, and prioritization frameworks.

**Process:**
1. Map the primary user flow as a Mermaid flowchart
2. Identify decision points, error states, and edge cases
3. Layer emotional states onto a journey map
4. Prioritize features against user goals and effort

### Phase 3: Architecture

Design the structural skeleton of the product.

**Artifacts produced:**
- Site map / screen inventory
- Navigation model
- Content hierarchy
- State mapping (what data appears where, in what states)

Load `references/ia-patterns.md` for navigation patterns, content hierarchy templates, and state mapping.

**Process:**
1. List every screen/page the product needs
2. Define the navigation model (tabs, sidebar, breadcrumbs, etc.)
3. Map content hierarchy within key screens
4. Document states: empty, loading, populated, error, edge cases

### Phase 4: Specification

Produce documents that a developer or designer can build from.

**Artifacts produced:**
- Design brief (one-pager summarizing the project)
- Component requirements (what each component does, its states, its data)
- Accessibility checklist (WCAG 2.2 AA minimum)
- Developer handoff notes

Load `references/specification-templates.md` for brief format, component spec structure, WCAG checklist, and handoff template.

**Process:**
1. Write a design brief summarizing discovery through architecture
2. Spec out key components with states, interactions, and data requirements
3. Run through the accessibility checklist
4. Produce handoff notes with implementation priorities

### Phase 5: Critique

Evaluate an existing design or the design produced in previous phases.

**Artifacts produced:**
- Heuristic evaluation scorecard (based on Nielsen's heuristics, modernized)
- Accessibility audit findings
- Design consistency report
- Prioritized improvement recommendations

Load `references/critique-frameworks.md` for heuristic definitions, scoring rubric, and audit checklist.

**Process:**
1. Score each heuristic 1-5 with specific evidence
2. Run an accessibility audit against WCAG 2.2 AA
3. Check consistency: typography scale, spacing system, color usage, component patterns
4. Rank issues by severity and effort to fix

## Output Format

All artifacts use markdown with:
- **Mermaid diagrams** for flows and architectures (```mermaid code blocks)
- **Tables** for matrices and comparisons
- **Headings** for document structure
- **Bold callouts** for assumptions and open questions

When producing multiple artifacts, use clear `## Section` headers so the output is scannable.

## Working with other skills

Design-strategy outputs are designed to feed into implementation skills:
- **Design briefs → frontend-design**: The brief provides the "why" and constraints; frontend-design provides the "how"
- **Component specs → frontend-design**: Specs define behavior and states; frontend-design implements the visuals
- **User flows → any implementation skill**: Flows define the happy path and edge cases to build for

When the user is ready to move from strategy to implementation, suggest they invoke the appropriate implementation skill with the artifacts produced here as context.
