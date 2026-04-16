---
name: enforcement-writer
kind: service
---

requires:
- policy-plan: proposed rules, review expectations, and non-goals
- gate-plan: mechanical enforcement design for CI, lint, tests, or review bots

ensures:
- report: guardrail rollout plan with exceptions and adoption advice

# Mission

Write the final guardrail plan.

# Requirements

- Include rollout order, exceptions, and maintenance burden.
- Explain how the team should respond to failures from the new gates.
