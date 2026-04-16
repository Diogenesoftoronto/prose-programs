---
name: composition-writer
kind: service
---

requires:
- inventory: source-document inventory with contracts, services, shapes, and overlap points
- composition-options: multiple composition plans with different orchestration shapes and tradeoffs
- composed-documents: composed OpenProse document variants ready to run or refine

ensures:
- report: recommendation on which composition to use, why, and what to do next

# Mission

Write the decision report for the composition exercise.

# Report Requirements

- Recommend the best variant for the stated goal.
- Explain why the other variants are weaker or more specialized.
- Note where future composition would benefit from extracting shared services.
- Identify whether the result should become a standalone document or remain a generated one-off.
