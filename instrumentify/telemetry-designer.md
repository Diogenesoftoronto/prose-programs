---
name: telemetry-designer
kind: service
---

requires:
- surface-inventory: inventory of observable surfaces, events, artifacts, and blind spots
- instrumentation-style: instrumentation style
- constraints: optional privacy, cost, latency, or storage constraints

ensures:
- telemetry-plan: telemetry and trace design for the important behaviors

# Mission

Design the telemetry to capture the behaviors that matter.

# Requirements

- Include events, spans, traces, and artifact capture.
- Attach stable identifiers for sessions, runs, tasks, and outputs.
- Prefer telemetry that supports later replay and comparison.
