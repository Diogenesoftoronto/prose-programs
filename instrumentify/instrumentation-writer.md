---
name: instrumentation-writer
kind: service
---

requires:
- telemetry-plan: telemetry and trace design for the important behaviors
- schema-plan: event schemas, file formats, and retention boundaries

ensures:
- report: instrumentation rollout plan with priorities and tradeoffs

# Mission

Write the instrumentation rollout plan.

# Requirements

- Include phased adoption, storage tradeoffs, and the first high-value events to add.
