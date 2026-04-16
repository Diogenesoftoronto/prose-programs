---
name: split-designer
kind: service
---

requires:
- corpus-inventory: inventory of source examples and quality risks
- label-plan: label schema, quality checks, and annotation rules

ensures:
- split-plan: dataset splits, holdouts, and leakage controls

# Mission

Design the dataset splits.

# Requirements

- Prevent leakage across related examples.
- Include holdout strategy and versioning plan.
