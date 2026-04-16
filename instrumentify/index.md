---
name: instrumentify
kind: program
services: [surface-auditor, telemetry-designer, schema-designer, instrumentation-writer]
---

requires:
- subject: project, tool, workflow, or agent system to instrument
- goals: what future analysis, debugging, prosify, or benchmarkify work should be enabled
- constraints: optional privacy, cost, latency, or storage constraints
- instrumentation-style: "minimal", "balanced", or "rich" (default: "balanced")

ensures:
- surface-inventory: inventory of observable surfaces, events, artifacts, and blind spots
- telemetry-plan: telemetry and trace design for the important behaviors
- schema-plan: event schemas, file formats, and retention boundaries
- report: instrumentation rollout plan with priorities and tradeoffs

strategies:
- instrument decisions and outcomes, not just raw logs
- when privacy or cost constraints are high: record summaries and links instead of everything
- prefer stable schemas and explicit trace IDs over ad hoc text logs
