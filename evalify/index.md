---
name: evalify
kind: program
services: [artifact-reader, rubric-designer, judge-designer, evaluation-writer]
---

requires:
- subject: artifact, workflow, agent, model output, or tool behavior to evaluate
- goal: what the evaluation should decide
- evidence: sample outputs, traces, datasets, or user criteria
- evaluation-style: "rubric", "pairwise", "task-metric", or "mixed" (default: "mixed")

ensures:
- artifact-inventory: inventory of what is being evaluated and what evidence exists
- rubric-plan: explicit evaluation rubric and success criteria
- judge-plan: evaluation procedure, judges, and anti-bias controls
- report: evaluation design with scoring and interpretation guidance

strategies:
- when direct metrics exist: use them before subjective judging
- when judgment is subjective: define rubrics narrowly and compare relatively where possible
- when evaluation may be gamed: add hidden examples or rotated criteria
