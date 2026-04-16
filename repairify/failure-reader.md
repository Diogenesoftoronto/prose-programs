---
name: failure-reader
kind: service
---

requires:
- subject: failing project, broken workflow, flaky test, bad session, incident, or regression to repair
- evidence: logs, failing tests, traces, repro steps, transcripts, or issue context

ensures:
- failure-inventory: inventory of failures, repro conditions, and impact

# Mission

Collect the failure evidence needed for a serious repair.

# Requirements

- Capture symptoms, scope, severity, and known repro steps.
- Separate confirmed failures from suspicions.
- Note missing evidence explicitly.
- Identify whether the failure is deterministic, flaky, or environmental.
