---
name: fix-plan-designer
kind: service
---

requires:
- failure-inventory: inventory of failures, repro conditions, and impact
- root-cause-plan: root-cause model with likely causes and confidence

ensures:
- repair-plan: ordered repair and validation plan

# Mission

Turn the root-cause analysis into a concrete repair sequence.

# Requirements

- Specify the fix order.
- Separate repair work from validation work.
- Include rollback or containment when relevant.
- Prefer changes that simplify the failing surface.
