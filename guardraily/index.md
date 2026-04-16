---
name: guardraily
kind: program
services: [risk-reader, policy-designer, gate-designer, enforcement-writer]
---

requires:
- subject: project, workflow, repository, or system that needs durable guardrails
- risks: optional list of repeated mistakes, regressions, or policy failures
- enforcement-style: "light", "balanced", or "strict" (default: "balanced")

ensures:
- risk-inventory: inventory of repeat failure patterns and enforcement targets
- policy-plan: proposed rules, review expectations, and non-goals
- gate-plan: mechanical enforcement design for CI, lint, tests, or review bots
- report: guardrail rollout plan with exceptions and adoption advice

strategies:
- when a rule cannot be enforced mechanically: keep it advisory, not mandatory
- when strict rules would cause thrash: phase them in behind a baseline cleanup
- prefer a small number of high-signal guardrails over policy sprawl
