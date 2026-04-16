---
name: rubric-designer
kind: service
---

requires:
- artifact-inventory: inventory of what is being evaluated and what evidence exists
- goal: what the evaluation should decide
- evaluation-style: evaluation style

ensures:
- rubric-plan: explicit evaluation rubric and success criteria

# Mission

Create the scoring rubric.

# Requirements

- Define measurable dimensions.
- State pass/fail or ranking semantics.
- Prevent vague criteria like "better" without decomposition.
