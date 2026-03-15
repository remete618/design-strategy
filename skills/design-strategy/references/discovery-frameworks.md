# Discovery Frameworks

## User Persona Template

```markdown
## Persona: [Name]

**Role:** [Job title or life role]
**Age range:** [e.g., 28-35]
**Tech comfort:** [Low / Medium / High]

### Goals
- [Primary goal — what success looks like for them]
- [Secondary goal]

### Frustrations
- [Pain point with current solutions]
- [Friction they experience regularly]

### Context
- [How they currently solve this problem]
- [Tools they already use]
- [When/where they encounter this need]

### Quote
> "[A sentence this person might actually say about the problem]"

### Assumptions ⚠️
- [List anything assumed rather than validated]
```

Create 2-4 personas. Resist the urge to make them demographic stereotypes — focus on behavioral differences that affect design decisions. Two personas with identical needs but different demographics aren't two personas.

**Good differentiators:** frequency of use, technical skill, primary goal, context of use, willingness to pay, data volume.

**Bad differentiators:** age alone, gender alone, job title without behavioral context.

## Jobs-to-Be-Done (JTBD)

Frame problems as jobs the user is hiring your product to do.

### JTBD Statement Format

```
When [situation/trigger],
I want to [motivation/action],
so I can [expected outcome].
```

### Examples

```
When I'm reviewing my team's weekly progress,
I want to see blockers and completed items in one view,
so I can prepare for standup in under 2 minutes.
```

```
When a customer submits a support ticket,
I want to be notified immediately with context,
so I can respond before they escalate.
```

### Writing good JTBD statements
- Start from the trigger situation, not the feature
- The motivation should be an action, not a feature name ("see blockers" not "use the dashboard")
- The outcome should be measurable or clearly observable
- Write 3-5 core jobs — if you have more than 8, you're describing features, not jobs

## Competitive Analysis Matrix

```markdown
| Feature / Aspect     | Our Product | Competitor A | Competitor B | Competitor C |
|---------------------|-------------|-------------|-------------|-------------|
| Core value prop      |             |             |             |             |
| Primary audience     |             |             |             |             |
| Onboarding time      |             |             |             |             |
| Key differentiator   |             |             |             |             |
| Pricing model        |             |             |             |             |
| Biggest weakness     |             |             |             |             |
| [Domain-specific 1]  |             |             |             |             |
| [Domain-specific 2]  |             |             |             |             |
```

### How to use this
- Fill in what's known, mark unknowns with `?`
- Focus on aspects that influence design decisions — skip marketing fluff
- Look for gaps: what does nobody do well? That's your opportunity
- Look for table stakes: what does everyone do? You need feature parity there
