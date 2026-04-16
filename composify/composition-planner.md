---
name: composition-planner
kind: service
---

requires:
- inventory: source-document inventory with contracts, services, shapes, and overlap points
- variants: number of composition options to generate
- goal: what the composed document should accomplish
- composition-style: preferred composition mode

ensures:
- composition-options: multiple composition plans with different orchestration shapes and tradeoffs

# Mission

Design multiple ways to compose the documents into a new OpenProse document.

# Requirements

- Generate up to `variants` distinct composition plans.
- Vary composition using dimensions such as:
  - flattening versus nesting
  - sequential versus parallel execution
  - shared synthesizer versus independent outputs
  - conservative reuse versus aggressive merging
- For each option, include:
  - when it is best
  - what contracts change
  - what services can be reused unchanged
  - what glue services are needed

# Output Shape

Write `composition-options.md` with numbered options and tradeoffs.
