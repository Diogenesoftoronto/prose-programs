---
name: sync-assessor
kind: service
---

requires:
- fleet-inventory: inventory of repositories, remotes, branch state, and local blockers across the fleet
- sync-policy: desired sync behavior
- upstream-branch: canonical upstream branch to check

ensures:
- sync-assessment: per-repo assessment of syncability, divergence, stale tracking data, and review risk

# Mission

Determine which repositories can be synchronized safely and which ones need review, cleanup, or fresh remote data first.

# Requirements

- For each repository, classify:
  - can fast-forward now
  - maybe can fast-forward after fetch
  - diverged
  - blocked by local state
  - not enough evidence
- Explain whether the verdict is based on:
  - fresh remote knowledge
  - existing local tracking refs
  - incomplete repository metadata
- Note review-sensitive upstream change surfaces when available.
- Avoid pretending a batch command is safe when repository states differ materially.

# Output Shape

Write `sync-assessment.md` with:

- per-repo verdicts
- confidence level and evidence source
- divergence or blocker notes
- likely review hotspots
- repositories safe to batch together
