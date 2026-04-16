---
name: gate-designer
kind: service
---

requires:
- risk-inventory: inventory of repeat failure patterns and enforcement targets
- policy-plan: proposed rules, review expectations, and non-goals

ensures:
- gate-plan: mechanical enforcement design for CI, lint, tests, or review bots

# Mission

Translate the rules into enforceable gates.

# Requirements

- Specify which rules belong in lint, tests, CI, presubmit, or review automation.
- Include baseline strategy for existing debt.
- Prefer deterministic checks over heuristic nags.
