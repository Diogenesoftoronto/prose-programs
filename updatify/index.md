---
name: updatify
kind: program
services: [repo-auditor, upstream-reader, merge-planner, update-writer]
---

requires:
- project: repository path, cloned project directory, or repo brief to update
- upstream-branch: upstream branch to reconcile against, such as "main" or "master" (default: "main")
- local-branch: local branch to update, such as the current branch or a long-lived integration branch (optional)
- update-policy: desired update style -- "aware-ff-only", "strict-ff-only", "rebase-assisted", or "report-only" (default: "aware-ff-only")
- risk-appetite: how aggressively to prepare update steps -- "conservative", "balanced", or "assertive" (default: "conservative")

ensures:
- local-state: inventory of the local repository state, branch topology, working tree cleanliness, and update blockers
- upstream-state: inventory of relevant upstream branch state, change clusters, and likely impact surfaces
- update-plan: step-by-step reconciliation plan that preserves safety and explains whether a real fast-forward is possible
- report: practical update report explaining what can be updated automatically, what must be handled manually, and why

strategies:
- when the local branch is a true ancestor of upstream: prefer explicit fast-forward update steps and post-update verification
- when uncommitted or untracked work exists: treat working tree hygiene as a blocker before any branch movement
- when histories have diverged: do not pretend an ff-only merge is available; explain the exact divergence and recommend the least risky next path
- when upstream changes touch fragile surfaces: group changes into impact clusters so the update plan reflects real review work instead of raw commit volume
- when the repository is hard to update safely: produce a report-only plan with commands, checkpoints, and rollback notes rather than speculative automation
