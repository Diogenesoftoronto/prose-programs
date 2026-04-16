---
name: sync-writer
kind: service
---

requires:
- fleet-inventory: inventory of repositories, remotes, branch state, and local blockers across the fleet
- sync-assessment: per-repo assessment of syncability, divergence, stale tracking data, and review risk
- sync-plan: prioritized synchronization plan with per-repo commands, checkpoints, and batching guidance

ensures:
- report: practical fleet sync report explaining what can be updated now, what is blocked, and what should be synchronized first

# Mission

Write a fleet-level sync report that an operator can act on without hiding repo-specific risk.

# Requirements

- Explain:
  - which repositories are safe to synchronize now
  - which need fetch, cleanup, or branch review first
  - where conclusions are limited by stale tracking information
  - what order to execute commands in
- Keep per-repo commands short and explicit.
- Include a clear section for repositories that should not be changed yet.
- Prefer operational clarity over exhaustive prose.

# Output Shape

Write `report.md` with:

- executive verdict
- safe-now repositories
- blocked or uncertain repositories
- recommended sync order
- command checklist
- escalation notes
