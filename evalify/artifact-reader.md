---
name: artifact-reader
kind: service
---

requires:
- subject: artifact, workflow, agent, model output, or tool behavior to evaluate
- evidence: sample outputs, traces, datasets, or user criteria

ensures:
- artifact-inventory: inventory of what is being evaluated and what evidence exists

# Mission

Understand the thing being evaluated and the evidence available.

# Requirements

- Capture output types, tasks, constraints, and observable behaviors.
- Separate evaluation targets from side effects like latency or cost.
- Identify missing evidence that blocks a fair evaluation.
