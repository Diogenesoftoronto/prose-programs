---
name: regression-writer
kind: service
---

requires:
- failure-inventory: inventory of failures, repro conditions, and impact
- repair-plan: ordered repair and validation plan

ensures:
- report: practical repair report with fixes and regression guards

# Mission

Write the final repair report.

# Requirements

- Include repro, repair, validation, and guardrails.
- Explain what should be tested so the failure does not return.
- State any residual uncertainty.
