---
name: trace-writer
kind: service
---

requires:
- schema-plan: normalized trace schema and identity model
- normalization-plan: ingestion, conversion, and retention plan

ensures:
- report: trace normalization report with output layout and next steps

# Mission

Write the trace normalization report.

# Requirements

- Include schema, output layout, and what downstream systems it unlocks.
