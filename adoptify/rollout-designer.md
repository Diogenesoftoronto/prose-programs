---
name: rollout-designer
kind: service
---

requires:
- context-inventory: inventory of current environment, constraints, and adoption risks
- change-plan: what must change technically and organizationally

ensures:
- rollout-plan: rollout stages, training, and fallback plan

# Mission

Design the rollout.

# Requirements

- Include pilot scope, graduation criteria, fallback path, and owner responsibilities.
