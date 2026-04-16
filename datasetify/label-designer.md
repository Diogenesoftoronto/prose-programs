---
name: label-designer
kind: service
---

requires:
- corpus-inventory: inventory of source examples and quality risks
- labeling-style: labeling style

ensures:
- label-plan: label schema, quality checks, and annotation rules

# Mission

Design the labels and annotation rules.

# Requirements

- Define labels, edge cases, and quality checks.
- Specify confidence handling and disagreement resolution.
