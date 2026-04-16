---
name: surface-auditor
kind: service
---

requires:
- subject: project, tool, workflow, or agent system to instrument
- goals: what future analysis, debugging, prosify, or benchmarkify work should be enabled

ensures:
- surface-inventory: inventory of observable surfaces, events, artifacts, and blind spots

# Mission

Find what can and cannot currently be observed.

# Requirements

- List user-visible actions, internal decisions, tool calls, outputs, and state changes.
- Identify blind spots that block scientific debugging or benchmarking.
- Distinguish operational telemetry from research telemetry.
