---
name: stability-writer
kind: service
---

requires:
- determinism-plan: plan to reduce nondeterminism and flakiness
- environment-plan: environment and tooling stabilization plan

ensures:
- report: stabilization plan with verification strategy

# Mission

Write the stabilization report.

# Requirements

- Include proof criteria for declaring the system meaningfully more stable.
