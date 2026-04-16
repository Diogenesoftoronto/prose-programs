---
name: root-cause-designer
kind: service
---

requires:
- failure-inventory: inventory of failures, repro conditions, and impact
- repair-style: repair style

ensures:
- root-cause-plan: root-cause model with likely causes and confidence

# Mission

Design the root-cause investigation.

# Requirements

- Produce ranked hypotheses with evidence for and against each.
- Distinguish triggering condition from underlying design flaw.
- Call out what experiment or check would disambiguate each hypothesis.
