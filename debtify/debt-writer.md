---
name: debt-writer
kind: service
---

requires:
- priority-model: prioritization model with cost, payoff, and risk
- execution-plan: sequenced plan for paying debt down

ensures:
- report: debt reduction report with rationale and next steps

# Mission

Write the debt report.

# Requirements

- Include why this debt matters, not just what it is.
- Recommend the next debt item to attack.
