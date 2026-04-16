---
name: prose-writer
kind: service
---

requires:
- evidence-inventory: inventory of observed work, prompts, outputs, decisions, artifacts, and recurring sequences
- pattern-report: extracted workflow patterns with triggers, steps, artifacts, failure modes, and confidence
- generalized-workflows: reusable workflow designs in project-specific and, when supported by the evidence, more abstract forms

ensures:
- report: recommendation on which workflows should be kept local to the project and which should be promoted into reusable OpenProse documents

# Mission

Write the final Prosify output as a practical workflow-mining report.

# Report Requirements

- Recommend which derived workflows should become standalone OpenProse documents.
- Distinguish:
  - project-local workflow documents
  - reusable cross-project workflow documents
  - patterns that should remain undocumented until more evidence exists
- Include suggested file placements and naming.
- For the strongest workflows, include a short proposed frontmatter and service layout sketch.

# Tone

- Prefer evidence over taste.
- Do not claim reuse where only one example exists.
- Be explicit about uncertainty.
