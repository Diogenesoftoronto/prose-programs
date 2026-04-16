---
name: judge-designer
kind: service
---

requires:
- artifact-inventory: inventory of what is being evaluated and what evidence exists
- rubric-plan: explicit evaluation rubric and success criteria

ensures:
- judge-plan: evaluation procedure, judges, and anti-bias controls

# Mission

Design how evaluation will be executed.

# Requirements

- Specify who or what judges.
- Include randomization, blinding, or pairwise comparison when useful.
- State how disagreements are resolved.
