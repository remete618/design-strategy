# Critique Frameworks

## Heuristic Evaluation (Modernized Nielsen's Heuristics)

Score each heuristic 1-5 with specific evidence from the design being evaluated.

**Scoring:**
- **5** — Excellent: Best-practice implementation, delightful details
- **4** — Good: Solid implementation, minor improvements possible
- **3** — Adequate: Works but has noticeable friction
- **2** — Poor: Significant usability issues, likely causes user frustration
- **1** — Failing: Fundamentally broken or missing

### The 10 Heuristics

```markdown
## Heuristic Evaluation: [Product/Feature Name]

| # | Heuristic | Score | Evidence |
|---|-----------|-------|----------|
| 1 | **Visibility of system status** — Users always know what's happening. Loading states, progress indicators, confirmation feedback, sync status. | /5 | [Specific observations] |
| 2 | **Match between system and real world** — Language, concepts, and flow match user expectations, not internal jargon. Icons are intuitive. Metaphors are consistent. | /5 | [Specific observations] |
| 3 | **User control and freedom** — Easy undo/redo. Clear exits from flows. No dead ends. Users can change their minds without penalty. | /5 | [Specific observations] |
| 4 | **Consistency and standards** — UI patterns are consistent internally and match platform conventions. Same action = same result everywhere. | /5 | [Specific observations] |
| 5 | **Error prevention** — Design prevents errors before they happen. Confirmation for destructive actions. Smart defaults. Inline validation. Constraints on input. | /5 | [Specific observations] |
| 6 | **Recognition rather than recall** — Information is visible when needed, not memorized. Recently used items, contextual help, visible options over hidden menus. | /5 | [Specific observations] |
| 7 | **Flexibility and efficiency** — Shortcuts for power users without confusing beginners. Keyboard shortcuts, bulk actions, saved preferences, customizable workflows. | /5 | [Specific observations] |
| 8 | **Aesthetic and minimalist design** — Every element earns its place. No visual noise. Information hierarchy is clear. Content density matches the context. | /5 | [Specific observations] |
| 9 | **Help users recognize, diagnose, and recover from errors** — Error messages are specific, human-readable, and suggest a fix. No error codes without context. | /5 | [Specific observations] |
| 10 | **Help and documentation** — Contextual help is available where needed. Onboarding covers key concepts. Documentation is findable and current. | /5 | [Specific observations] |

**Overall Score: [X]/50**

### Summary
[2-3 sentences: overall assessment, biggest strengths, most critical issues]
```

### Interpreting Scores
- **45-50:** Production-ready, polished experience
- **35-44:** Solid foundation, specific areas need attention
- **25-34:** Usable but significant friction — prioritize improvements
- **15-24:** Major usability problems — needs redesign of key flows
- **Below 15:** Fundamental issues — step back and re-examine core approach

## Accessibility Audit

Go beyond the checklist — test the actual experience.

```markdown
## Accessibility Audit: [Product/Feature Name]

### Testing Method
- [ ] Keyboard-only navigation test
- [ ] Screen reader test (VoiceOver / NVDA / JAWS)
- [ ] High contrast mode
- [ ] 200% zoom
- [ ] Reduced motion preference
- [ ] Color blindness simulation (protanopia, deuteranopia, tritanopia)

### Findings

| Severity | Issue | Location | WCAG Criterion | Recommendation |
|----------|-------|----------|---------------|----------------|
| Critical | [Issue] | [Where] | [e.g., 1.4.3] | [Fix] |
| Major | [Issue] | [Where] | [Criterion] | [Fix] |
| Minor | [Issue] | [Where] | [Criterion] | [Fix] |

### Severity Definitions
- **Critical:** Blocks access entirely for some users (e.g., keyboard trap, missing form labels, no alt text on functional images)
- **Major:** Significant barrier that requires workarounds (e.g., poor contrast, missing focus indicators, unclear error messages)
- **Minor:** Inconvenience that doesn't block access (e.g., missing skip link, suboptimal reading order, decorative images with alt text)
```

## Design Consistency Report

Check whether the design follows its own rules consistently.

```markdown
## Consistency Report: [Product/Feature Name]

### Typography
| Usage | Font | Size | Weight | Line Height | Consistent? |
|-------|------|------|--------|-------------|-------------|
| H1 | | | | | ✅/❌ |
| H2 | | | | | ✅/❌ |
| Body | | | | | ✅/❌ |
| Caption | | | | | ✅/❌ |
| Button | | | | | ✅/❌ |

### Spacing System
- [ ] Consistent spacing scale (e.g., 4px base: 4, 8, 12, 16, 24, 32, 48)
- [ ] Margins and padding follow the scale
- [ ] Component spacing is predictable

### Color Usage
| Role | Value | Usage | Consistent? |
|------|-------|-------|-------------|
| Primary | | [Where used] | ✅/❌ |
| Secondary | | [Where used] | ✅/❌ |
| Success | | [Where used] | ✅/❌ |
| Warning | | [Where used] | ✅/❌ |
| Error | | [Where used] | ✅/❌ |
| Neutral/Text | | [Where used] | ✅/❌ |

### Component Patterns
| Pattern | Instances | Consistent? | Notes |
|---------|-----------|-------------|-------|
| Buttons | [List locations] | ✅/❌ | [Inconsistencies found] |
| Form inputs | | ✅/❌ | |
| Cards | | ✅/❌ | |
| Modals/Dialogs | | ✅/❌ | |
| Tables | | ✅/❌ | |
| Navigation | | ✅/❌ | |

### Inconsistencies Found
1. [Issue] — [Where] — [Recommendation]
2. [Issue] — [Where] — [Recommendation]
```

## Prioritized Improvement Recommendations

After completing the evaluation, synthesize findings into an actionable list.

```markdown
## Improvement Recommendations: [Product/Feature Name]

### Critical (fix before launch / immediately)
1. **[Issue]** — [Impact on users] — [Suggested fix]
2. **[Issue]** — [Impact on users] — [Suggested fix]

### High Priority (fix in next sprint)
1. **[Issue]** — [Impact on users] — [Suggested fix]
2. **[Issue]** — [Impact on users] — [Suggested fix]

### Medium Priority (fix in next cycle)
1. **[Issue]** — [Impact on users] — [Suggested fix]

### Low Priority (backlog)
1. **[Issue]** — [Impact on users] — [Suggested fix]

### Strengths to Preserve
- [What's working well — don't break these in the process of fixing issues]
- [Specific positive patterns to maintain]
```
