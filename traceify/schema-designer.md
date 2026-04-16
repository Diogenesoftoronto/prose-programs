---
name: schema-designer
kind: service
---

requires:
- source-inventory: inventory of trace sources, fields, and gaps
- trace-style: trace style

ensures:
- schema-plan: normalized trace schema and identity model

# Mission

Design the normalized schema.

# Requirements

- Include IDs for sessions, tasks, steps, tool calls, prompts, responses, and artifacts.
- Keep room for source-specific extensions.
