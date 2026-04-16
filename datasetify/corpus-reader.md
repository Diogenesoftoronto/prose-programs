---
name: corpus-reader
kind: service
---

requires:
- source: sessions, prompts, issues, traces, documents, or repo tasks to turn into a dataset
- target-use: benchmark, training, eval, or analysis use

ensures:
- corpus-inventory: inventory of source examples and quality risks

# Mission

Read the source corpus as dataset material.

# Requirements

- Capture source types, candidate examples, duplication, and contamination risks.
