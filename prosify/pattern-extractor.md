---
name: pattern-extractor
kind: service
---

requires:
- evidence-inventory: inventory of observed work, prompts, outputs, decisions, artifacts, and recurring sequences
- scope: whether to derive workflows for a specific project, a family of similar projects, or abstract reusable patterns

ensures:
- pattern-report: extracted workflow patterns with triggers, steps, artifacts, failure modes, and confidence

# Mission

Turn raw evidence into candidate workflow patterns.

# Requirements

- Identify workflows that recur across the evidence.
- For each workflow, capture:
  - trigger
  - required inputs
  - decision points
  - ordered or parallel steps
  - outputs and artifacts
  - typical failure modes
  - confidence level
- Separate:
  - project-specific workflows
  - potentially portable workflows
  - patterns that are too weak or too one-off to promote

# Output Shape

Write `pattern-report.md` with one section per candidate workflow.
