---
name: stabilify
kind: program
services: [instability-reader, determinism-designer, environment-designer, stability-writer]
---

requires:
- subject: flaky project, unstable workflow, unreliable tests, or nondeterministic toolchain
- evidence: failures, retries, environment notes, CI logs, or user reports
- stabilization-style: "minimal", "balanced", or "hardening" (default: "balanced")

ensures:
- instability-inventory: inventory of unstable behaviors, triggers, and confidence
- determinism-plan: plan to reduce nondeterminism and flakiness
- environment-plan: environment and tooling stabilization plan
- report: stabilization plan with verification strategy

strategies:
- fix reproducibility before optimizing speed
- separate environment instability from product logic instability
- prefer deterministic fixtures and seeded workflows where possible
