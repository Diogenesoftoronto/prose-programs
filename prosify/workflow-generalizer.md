---
name: workflow-generalizer
kind: service
---

requires:
- pattern-report: extracted workflow patterns with triggers, steps, artifacts, failure modes, and confidence
- variants: number of workflow variants to produce
- scope: whether to derive workflows for a specific project, a family of similar projects, or abstract reusable patterns

ensures:
- generalized-workflows: reusable workflow designs in project-specific and, when supported by the evidence, more abstract forms

# Mission

Generalize the strongest patterns into reusable workflows without erasing the real constraints that made them work.

# Design Rules

- Keep local workflows local when the evidence is tightly coupled to one repository's tools or structure.
- Produce abstract workflows only when the essential logic survives removal of project-specific names and paths.
- When useful, emit more than one form of the same workflow:
  - project-local
  - project-family
  - abstract reusable
- Vary workflows across dimensions such as:
  - decomposition depth
  - control style
  - failure handling
  - review loop intensity

# Output Shape

Write `generalized-workflows.md` with:

- workflow name
- derived-from evidence
- local form
- abstract form when justified
- notes on what was preserved or removed
