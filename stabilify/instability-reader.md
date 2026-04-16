---
name: instability-reader
kind: service
---

requires:
- subject: flaky project, unstable workflow, unreliable tests, or nondeterministic toolchain
- evidence: failures, retries, environment notes, CI logs, or user reports

ensures:
- instability-inventory: inventory of unstable behaviors, triggers, and confidence

# Mission

Catalog the unstable surfaces.

# Requirements

- Record where instability occurs, how often, and under what conditions.
- Distinguish true product failures from harness noise.
