---
name: migration-planner
kind: service
---

requires:
- inventory: inventory of the current project's architecture, tooling, critical constraints, and migration-sensitive components
- mapping: source-to-target capability map with substitutions, gaps, and compatibility notes
- migration-style: migration style

ensures:
- migration-plan: phased migration plan with milestones, fallback strategy, and cutover path

# Mission

Turn the stack mapping into a migration plan that can actually be executed.

# Planning Rules

- Prefer seam-first migrations over total rewrites when possible.
- Keep the old system serving value while the new system proves itself.
- Include rollback or fallback options.
- Distinguish:
  - preparatory work
  - bridge work
  - feature parity work
  - cutover work
  - cleanup work

# Output Shape

Write `migration-plan.md` with:

- phases
- milestones
- risks
- compatibility strategy
- cutover strategy
- cleanup after migration
