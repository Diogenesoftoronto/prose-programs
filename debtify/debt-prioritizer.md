---
name: debt-prioritizer
kind: service
---

requires:
- debt-inventory: inventory of debt items, sources, and drag
- debt-style: debt style

ensures:
- priority-model: prioritization model with cost, payoff, and risk

# Mission

Rank the debt items.

# Requirements

- Score each item by impact, urgency, implementation cost, and strategic value.
- Call out which debt is enabling debt versus cosmetic debt.
