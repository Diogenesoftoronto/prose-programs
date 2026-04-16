---
name: sequence-designer
kind: service
---

requires:
- debt-inventory: inventory of debt items, sources, and drag
- priority-model: prioritization model with cost, payoff, and risk

ensures:
- execution-plan: sequenced plan for paying debt down

# Mission

Turn prioritization into execution order.

# Requirements

- Sequence quick wins, enabling work, and structural work separately.
- Include validation and rollback considerations where relevant.
