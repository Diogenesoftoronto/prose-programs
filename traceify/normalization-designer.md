---
name: normalization-designer
kind: service
---

requires:
- source-inventory: inventory of trace sources, fields, and gaps
- schema-plan: normalized trace schema and identity model

ensures:
- normalization-plan: ingestion, conversion, and retention plan

# Mission

Design how raw traces become normalized traces.

# Requirements

- Specify ingestion order, conversion logic, validation, and retention classes.
- Preserve raw provenance.
