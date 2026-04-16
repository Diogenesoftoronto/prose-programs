---
name: schema-designer
kind: service
---

requires:
- surface-inventory: inventory of observable surfaces, events, artifacts, and blind spots
- telemetry-plan: telemetry and trace design for the important behaviors

ensures:
- schema-plan: event schemas, file formats, and retention boundaries

# Mission

Specify the schemas and storage rules.

# Requirements

- Define event shapes, file formats, trace bundles, and retention classes.
- State what must be versioned.
- Separate raw artifacts from derived summaries.
