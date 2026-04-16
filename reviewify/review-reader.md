---
name: review-reader
kind: service
---

requires:
- subject: PR, patch series, codebase slice, session, or workflow to review
- evidence: diffs, comments, traces, outputs, or conversation context

ensures:
- review-inventory: inventory of reviewed artifacts and context

# Mission

Gather the material needed for review.

# Requirements

- Record scope, changed surfaces, and relevant context.
- Distinguish raw artifact from commentary about it.
