---
name: risk-reader
kind: service
---

requires:
- subject: project, workflow, repository, or system that needs durable guardrails
- risks: optional list of repeated mistakes, regressions, or policy failures

ensures:
- risk-inventory: inventory of repeat failure patterns and enforcement targets

# Mission

Identify the failure patterns worth guarding against.

# Requirements

- Distinguish one-off mistakes from recurring classes of mistakes.
- Note which risks are code-level, review-level, CI-level, or release-level.
- Record the current cost of each failure class.
