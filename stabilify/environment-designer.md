---
name: environment-designer
kind: service
---

requires:
- instability-inventory: inventory of unstable behaviors, triggers, and confidence
- determinism-plan: plan to reduce nondeterminism and flakiness

ensures:
- environment-plan: environment and tooling stabilization plan

# Mission

Design the environment hardening work.

# Requirements

- Cover dev, CI, and release environments.
- Specify pinned versions, caches, setup checks, and environment assertions.
