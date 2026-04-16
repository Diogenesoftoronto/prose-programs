---
name: frameworkify
kind: program
services: [project-reader, abstraction-designer, packaging-designer, framework-writer]
---

requires:
- project: repository path, project directory, or project brief to frameworkify
- target-ecosystem: target package ecosystem for reusable output, such as npm, crates.io, PyPI, or internal monorepo packages (optional)
- cli-style: desired starter CLI style, such as interactive, non-interactive, or both (default: "both")
- appetite: how aggressive the extraction should be -- "conservative", "balanced", or "maximal" (default: "balanced")

ensures:
- inventory: clear inventory of the project's domain problems, core capabilities, tech choices, and extraction candidates
- framework-plan: reusable framework design describing modules, boundaries, extension points, and what remains app-specific
- starter-spec: easy project bootstrap CLI design, including commands, inputs, templates, and defaults
- report: a practical frameworkification report with extraction order, risks, and recommended first cuts

strategies:
- when the project mixes product logic and framework logic: separate stable domain primitives before extracting UI or infra wrappers
- when frameworkification would create artificial abstraction: recommend keeping code local instead of exporting it
- when a CLI should serve multiple audiences: provide both a fast-path starter and an advanced scaffold path
