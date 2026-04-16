---
name: migration-writer
kind: service
---

requires:
- inventory: inventory of the current project's architecture, tooling, critical constraints, and migration-sensitive components
- mapping: source-to-target capability map with substitutions, gaps, and compatibility notes
- migration-plan: phased migration plan with milestones, fallback strategy, and cutover path

ensures:
- report: migration report with recommendation, tradeoffs, and first milestones

# Mission

Write the final migration decision report.

# Report Requirements

- State whether the migration is worth doing.
- Explain the safest migration style.
- Identify the first code moves or experiments to run.
- Name the biggest unknowns that must be validated before committing fully.
- Include explicit non-goals so the migration does not expand into a vanity rewrite.
