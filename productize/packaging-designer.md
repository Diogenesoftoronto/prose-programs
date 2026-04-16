---
name: packaging-designer
kind: service
---

requires:
- readiness-inventory: readiness audit covering gaps between current state and usable product state
- distribution: how the product should be delivered
- productization-style: productization style

ensures:
- packaging-plan: product packaging and distribution design

# Mission

Design the packaging and delivery model.

# Requirements

- Specify what gets packaged, how it is installed, and how it is updated.
- Include pricing or access boundary assumptions when relevant.
