---
name: syncify
kind: program
services: [fleet-reader, sync-assessor, priority-planner, sync-writer]
---

requires:
- projects: list of repository paths, a root directory containing cloned repositories, or a repo fleet brief to synchronize
- upstream-branch: canonical upstream branch to check, such as "main" or "master" (default: "main")
- sync-policy: desired sync behavior -- "aware-ff-only", "strict-ff-only", "rebase-assisted", "report-only", or "mixed" (default: "aware-ff-only")
- freshness-goal: how aggressively to reduce drift -- "daily", "weekly", "on-demand", or "release-driven" (default: "on-demand")
- risk-appetite: how aggressively to prepare sync steps -- "conservative", "balanced", or "assertive" (default: "conservative")

ensures:
- fleet-inventory: inventory of repositories, remotes, branch state, and local blockers across the fleet
- sync-assessment: per-repo assessment of syncability, divergence, stale tracking data, and review risk
- sync-plan: prioritized synchronization plan with per-repo commands, checkpoints, and batching guidance
- report: practical fleet sync report explaining what can be updated now, what is blocked, and what should be synchronized first

strategies:
- when many repositories are present: separate repos that are clean fast-forward candidates from repos that need human attention
- when remote tracking data may be stale: label conclusions as based on local refs unless fresh upstream state is confirmed
- when repositories differ in risk: prioritize infrastructure, shared libraries, and active worktrees ahead of dormant clones
- when a batch sync would hide important differences: keep commands and blockers explicit per repository
- when a repository cannot be safely advanced: recommend report-only handling rather than speculative branch movement
