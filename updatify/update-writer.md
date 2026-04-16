---
name: update-writer
kind: service
---

requires:
- local-state: inventory of the local repository state, local changes, branch position, and update blockers
- upstream-state: inventory of the upstream branch state, relevant change clusters, and likely impact surfaces
- update-plan: chosen reconciliation plan with safety checks and fallback path

ensures:
- report: practical update report explaining what can be updated automatically, what must be handled manually, and why

# Mission

Turn repository state and branch logic into an operator-friendly update report.

# Requirements

- Explain:
  - whether the repository can be updated with a real fast-forward
  - what must be cleaned or preserved first
  - what upstream changes deserve focused review
  - which commands or checkpoints should be run
- Make the report operational, not theoretical.
- Prefer short command sequences with clear stop conditions.
- Include a "do not proceed yet" section when safety blockers exist.

# Output Shape

Write `report.md` with:

- executive verdict
- blockers and prerequisites
- recommended command sequence
- focused review areas
- verification checklist
- fallback or escalation notes
