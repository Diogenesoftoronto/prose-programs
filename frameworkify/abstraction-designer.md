---
name: abstraction-designer
kind: service
---

requires:
- inventory: project inventory covering problem domain, architecture, technologies, stable seams, and extraction candidates
- target-ecosystem: target package ecosystem for reusable output
- appetite: extraction aggressiveness

ensures:
- framework-plan: proposed reusable framework architecture with packages, interfaces, and extension points

# Mission

Design the reusable shape of the project without laundering product-specific assumptions into a fake framework.

# Design Rules

- Prefer extracting stable primitives over abstract base classes or generic managers.
- Keep product-specific policy out of the framework layer.
- Separate:
  - core domain library
  - adapters and integrations
  - UI kits or starter app pieces
  - generators or scaffolding
- Name the exact modules that should exist after extraction.
- For each module, state:
  - purpose
  - public API
  - dependencies
  - likely consumers
  - what must stay private

# Output Shape

Write `framework-plan.md` with:

- framework thesis
- package and module map
- extension points
- anti-goals
- extraction sequence
