---
name: trace-reader
kind: service
---

requires:
- source: logs, sessions, tool traces, prompt traces, CLI outputs, or mixed trace sources
- target-use: why the traces are being normalized

ensures:
- source-inventory: inventory of trace sources, fields, and gaps

# Mission

Read the trace sources and understand their structure.

# Requirements

- Capture source formats, key fields, correlations, and blind spots.
- Identify which trace fields are required for replay or comparison.
