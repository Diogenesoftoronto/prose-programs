---
name: fleet-reader
kind: service
---

requires:
- projects: list of repository paths, a root directory containing cloned repositories, or a repo fleet brief to synchronize
- upstream-branch: canonical upstream branch to check

ensures:
- fleet-inventory: inventory of repositories, remotes, branch state, and local blockers across the fleet

# Mission

Build a truthful picture of the repository fleet before proposing any batch synchronization work.

# Requirements

- Capture for each repository:
  - path and repository identity
  - current branch and default tracking branch
  - working tree cleanliness
  - configured remotes
  - presence of local-only commits or unpushed branches
  - evidence of stale or missing upstream tracking refs
- Distinguish repositories that are:
  - immediately assessable
  - missing critical git metadata
  - unsafe to touch without preserving local work
- Prefer simple, comparable facts across all repositories.

# Output Shape

Write `fleet-inventory.md` with:

- repository roster
- per-repo local state summary
- remote and tracking summary
- blockers and unknowns
- readiness groups
