---
name: debt-reader
kind: service
---

requires:
- subject: repository, system, or workflow with technical debt to analyze
- goals: optional business, engineering, or reliability goals

ensures:
- debt-inventory: inventory of debt items, sources, and drag

# Mission

Identify real technical debt and the drag it causes.

# Requirements

- Capture debt source, affected area, and current cost.
- Separate accidental complexity from deliberate tradeoffs.
- Note evidence for each debt item.
