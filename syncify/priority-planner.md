---
name: priority-planner
kind: service
---

requires:
- fleet-inventory: inventory of repositories, remotes, branch state, and local blockers across the fleet
- sync-assessment: per-repo assessment of syncability, divergence, stale tracking data, and review risk
- freshness-goal: desired drift reduction cadence
- risk-appetite: desired conservatism for sync execution

ensures:
- sync-plan: prioritized synchronization plan with per-repo commands, checkpoints, and batching guidance

# Mission

Turn mixed repository states into a practical sync queue instead of a dangerous one-liner.

# Requirements

- Prioritize repositories by:
  - safety to advance
  - operational importance
  - amount of drift
  - likely review cost
- Group repositories into:
  - safe now
  - safe after fetch or cleanup
  - manual review required
  - do not touch yet
- Provide explicit commands and stop conditions for each repository or batch.
- Include verification checkpoints after each sync step.

# Output Shape

Write `sync-plan.md` with:

- priority order
- batch groups
- per-repo command sequences
- verification checkpoints
- deferred items and reasons
