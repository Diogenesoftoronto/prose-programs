---
name: merge-planner
kind: service
---

requires:
- local-state: inventory of the local repository state, local changes, branch position, and update blockers
- upstream-state: inventory of the upstream branch state, relevant change clusters, and likely impact surfaces
- update-policy: desired update style
- risk-appetite: desired conservatism for update execution

ensures:
- update-plan: step-by-step reconciliation plan that preserves safety and explains whether a real fast-forward is possible

# Mission

Produce the least risky update path that still tells the truth about repository history.

# Requirements

- Decide explicitly whether a true fast-forward is possible.
- If fast-forward is possible:
  - produce exact preparation, update, and verification steps
  - include checkpoints for tests, build, and rollback awareness
- If fast-forward is not possible:
  - explain why in ancestry terms
  - recommend the least risky next path based on the chosen update policy
  - avoid masking divergence behind vague "just merge it" advice
- Prefer plans that preserve user work and make review boundaries obvious.

# Output Shape

Write `update-plan.md` with:

- update classification
- ancestry verdict
- required preparation steps
- exact update sequence
- post-update verification
- fallback path if the preferred route fails
