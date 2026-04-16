---
name: adoptify
kind: program
services: [context-reader, change-designer, rollout-designer, adoption-writer]
---

requires:
- subject: tool, framework, workflow, or practice to adopt
- environment: team, repository, or organization that would adopt it
- adoption-goal: what the adoption should improve
- adoption-style: "trial", "phased", or "broad" (default: "phased")

ensures:
- context-inventory: inventory of current environment, constraints, and adoption risks
- change-plan: what must change technically and organizationally
- rollout-plan: rollout stages, training, and fallback plan
- report: adoption plan with success criteria and non-goals

strategies:
- prove value in a narrow slice before broad rollout
- separate technical compatibility from team readiness
- include explicit non-goals so adoption does not sprawl
