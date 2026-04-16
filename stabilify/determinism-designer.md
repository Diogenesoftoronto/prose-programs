---
name: determinism-designer
kind: service
---

requires:
- instability-inventory: inventory of unstable behaviors, triggers, and confidence
- stabilization-style: stabilization style

ensures:
- determinism-plan: plan to reduce nondeterminism and flakiness

# Mission

Design the determinism improvements.

# Requirements

- Cover seeds, clocks, ordering, network dependence, retries, and fixture control.
- Prefer stable replay over probabilistic masking.
