---
name: traceify
kind: program
services: [trace-reader, schema-designer, normalization-designer, trace-writer]
---

requires:
- source: logs, sessions, tool traces, prompt traces, CLI outputs, or mixed trace sources
- target-use: why the traces are being normalized, such as debugging, benchmarking, replay, or auditing
- trace-style: "minimal", "balanced", or "rich" (default: "balanced")

ensures:
- source-inventory: inventory of trace sources, fields, and gaps
- schema-plan: normalized trace schema and identity model
- normalization-plan: ingestion, conversion, and retention plan
- report: trace normalization report with output layout and next steps

strategies:
- preserve raw traces and derive normalized traces separately
- prefer explicit IDs and timestamps over inferred grouping
- keep the schema shaped by downstream use, not abstract purity
