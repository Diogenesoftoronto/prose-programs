---
name: upstream-reader
kind: service
---

requires:
- project: repository path, cloned project directory, or repo brief to update
- upstream-branch: upstream branch to reconcile against

ensures:
- upstream-state: inventory of the upstream branch state, relevant change clusters, and likely impact surfaces

# Mission

Read upstream changes in a way that is useful for safe updating, not just for counting commits.

# Requirements

- Identify the canonical upstream remote and branch.
- Capture:
  - ahead or behind relationship against the local branch
  - commit ranges relevant to the update
  - files, modules, or packages most affected upstream
  - migrations, lockfile changes, config churn, and interface shifts
- Group upstream changes into reviewable impact clusters.
- Highlight changes that could invalidate local assumptions even if a fast-forward is technically possible.

# Output Shape

Write `upstream-state.md` with:

- upstream branch summary
- commit or range summary
- impact clusters
- notable risky changes
- verification implications
