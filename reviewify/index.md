---
name: reviewify
kind: program
services: [review-reader, finding-extractor, pattern-synthesizer, review-writer]
---

requires:
- subject: PR, patch series, codebase slice, session, or workflow to review
- evidence: diffs, comments, traces, outputs, or conversation context
- review-goal: what the review should prioritize
- review-style: "strict", "balanced", or "advisory" (default: "balanced")

ensures:
- review-inventory: inventory of reviewed artifacts and context
- findings: prioritized findings with severity and evidence
- patterns: repeated themes, classes of mistakes, and reusable review heuristics
- report: review report with recommendations and follow-up actions

strategies:
- findings first, summary second
- separate concrete bugs from stylistic disagreement
- promote repeated findings into reusable heuristics
