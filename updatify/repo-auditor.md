---
name: repo-auditor
kind: service
---

requires:
- project: repository path, cloned project directory, or repo brief to update
- local-branch: local branch to update

ensures:
- local-state: inventory of the local repository state, local changes, branch position, and update blockers

# Mission

Understand the local repository well enough to know whether any safe update path exists.

# Requirements

- Capture:
  - current branch and target local branch
  - cleanliness of tracked and untracked files
  - local commits not yet reflected upstream
  - local config or generated artifacts that may interfere with update work
  - existing tests, lockfiles, and deployment-sensitive surfaces
- Distinguish between:
  - harmless local dirt
  - update blockers
  - changes that must be preserved before branch movement
- Treat unresolved local state as a first-class part of the update problem.

# Output Shape

Write `local-state.md` with:

- branch and working tree status
- local-only commits or patches
- dirty-state blockers
- fragile files or generated artifacts
- readiness assessment
