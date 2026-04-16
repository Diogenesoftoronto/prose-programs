---
name: packaging-designer
kind: service
---

requires:
- inventory: project inventory covering problem domain, architecture, technologies, stable seams, and extraction candidates
- framework-plan: proposed reusable framework architecture with packages, interfaces, and extension points
- cli-style: desired starter CLI style
- target-ecosystem: target package ecosystem for reusable output

ensures:
- starter-spec: starter CLI and packaging specification for reusing the framework in new projects

# Mission

Specify how other people should adopt the extracted framework with the least ceremony.

# Requirements

- Design a CLI that can start a new project quickly.
- Include command names, arguments, defaults, and template choices.
- Specify how packages should be published or consumed.
- Prefer a minimal starter path that works in one command.
- Include upgrade and extension hooks, not just first-run scaffolding.

# Output Shape

Write `starter-spec.md` with:

- package publishing or distribution plan
- bootstrap CLI commands
- starter templates
- generated project layout
- customization hooks
- upgrade path
