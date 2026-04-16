---
name: prose-reader
kind: service
---

requires:
- documents: two or more OpenProse documents, program paths, or pasted document contents
- goal: what the composed document should accomplish

ensures:
- inventory: source-document inventory with contracts, services, shapes, and overlap points

# Mission

Read the input OpenProse documents and identify what can be recombined safely.

# Requirements

- For each document, capture:
  - purpose
  - requires
  - ensures
  - services or major blocks
  - strategies and assumptions
- Identify:
  - overlapping inputs
  - overlapping outputs
  - compatible services
  - conflicting assumptions
  - missing glue contracts

# Output Shape

Write `inventory.md` with:

- source summaries
- contract map
- overlap analysis
- composition hazards
