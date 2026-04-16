---
name: change-designer
kind: service
---

requires:
- context-inventory: inventory of current environment, constraints, and adoption risks
- adoption-style: adoption style

ensures:
- change-plan: what must change technically and organizationally

# Mission

Design the required change surface.

# Requirements

- Cover tooling, process, docs, and training changes.
- Separate required change from optional polish.
