---
name: finding-extractor
kind: service
---

requires:
- review-inventory: inventory of reviewed artifacts and context
- review-goal: what the review should prioritize
- review-style: review style

ensures:
- findings: prioritized findings with severity and evidence

# Mission

Extract the review findings.

# Requirements

- State severity, risk, and evidence.
- Prefer behavioral findings over preference-level notes.
