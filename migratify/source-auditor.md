---
name: source-auditor
kind: service
---

requires:
- project: repository path, project directory, or project brief to migrate
- migration-goal: what success means

ensures:
- inventory: inventory of the current project's architecture, tooling, critical constraints, and migration-sensitive components

# Mission

Understand the current system well enough to avoid fantasy migration plans.

# Requirements

- Capture:
  - language and framework stack
  - build and deploy tooling
  - runtime assumptions
  - data and API boundaries
  - test and release expectations
  - platform-specific features
- Identify the highest-risk migration surfaces.
- Separate core behavior from incidental tooling.

# Output Shape

Write `inventory.md` with:

- current stack
- architectural components
- hard constraints
- migration blockers
- candidate seams
