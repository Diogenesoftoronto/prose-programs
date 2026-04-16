---
name: project-reader
kind: service
---

requires:
- project: repository path, project directory, or project brief
- appetite: extraction aggressiveness

ensures:
- inventory: project inventory covering problem domain, architecture, technologies, stable seams, and extraction candidates

# Mission

Understand what the project actually does before proposing a reusable framework.

# Requirements

- Identify the real problems the project solves, not just the implementation details.
- List the technologies, tools, libraries, and deployment assumptions in use.
- Distinguish:
  - domain logic
  - product-specific UI or branding
  - infrastructure glue
  - reusable primitives
- Highlight candidate modules that could become libraries or packages.
- Highlight code that should remain application-specific.

# Output Shape

Write `inventory.md` with:

- project purpose
- recurring capabilities
- tech stack
- candidate reusable modules
- candidate non-reusable modules
- extraction risks
