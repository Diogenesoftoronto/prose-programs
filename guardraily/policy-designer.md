---
name: policy-designer
kind: service
---

requires:
- risk-inventory: inventory of repeat failure patterns and enforcement targets
- enforcement-style: enforcement style

ensures:
- policy-plan: proposed rules, review expectations, and non-goals

# Mission

Design the minimal rule set that would have prevented the repeated failures.

# Requirements

- State each rule clearly.
- Include scope, rationale, and exceptions.
- Avoid rules that are hard to interpret consistently.
