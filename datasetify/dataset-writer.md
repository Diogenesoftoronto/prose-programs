---
name: dataset-writer
kind: service
---

requires:
- label-plan: label schema, quality checks, and annotation rules
- split-plan: dataset splits, holdouts, and leakage controls

ensures:
- report: dataset design report with generation and maintenance plan

# Mission

Write the dataset report.

# Requirements

- Include provenance, quality plan, and update policy.
