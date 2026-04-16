---
name: repairify
kind: program
services: [failure-reader, root-cause-designer, fix-plan-designer, regression-writer]
---

requires:
- subject: failing project, broken workflow, flaky test, bad session, incident, or regression to repair
- evidence: logs, failing tests, traces, repro steps, transcripts, or issue context
- repair-style: "surgical", "balanced", or "systemic" (default: "balanced")

ensures:
- failure-inventory: inventory of failures, repro conditions, and impact
- root-cause-plan: root-cause model with likely causes and confidence
- repair-plan: ordered repair and validation plan
- report: practical repair report with fixes and regression guards

strategies:
- when the failure is not reproducible: prioritize reproducer design first
- when multiple root causes are possible: rank them instead of pretending certainty
- when a fix is risky: recommend the smallest reversible repair first
