---
name: prosify
kind: program
services: [evidence-reader, pattern-extractor, workflow-generalizer, prose-writer]
---

requires:
- source: repository path, git history, conversation log, prompt/result archive, or combined evidence source to analyze
- scope: whether to derive workflows for a specific project, for a family of similar projects, or as abstract reusable patterns (default: "project")
- focus: optional area to mine, such as debugging, release work, migration work, feature delivery, code review, incident response, or prompt patterns
- variants: number of workflow variants to produce when multiple reusable shapes are possible (default: 3)

ensures:
- evidence-inventory: inventory of observed work, prompts, outputs, decisions, artifacts, and recurring sequences
- pattern-report: extracted workflow patterns with triggers, steps, artifacts, failure modes, and confidence
- generalized-workflows: reusable workflow designs in project-specific and, when supported by the evidence, more abstract forms
- report: recommendation on which workflows should be kept local to the project and which should be promoted into reusable OpenProse documents

strategies:
- when prompt and result evidence is available: prefer direct workflow extraction from that evidence over inference from final code alone
- when only repository history is available: infer workflows cautiously and label confidence clearly
- when a pattern appears only once: keep it as a candidate, not a reusable workflow
- when a workflow depends on project-specific tooling or paths: emit both a local version and a generalized version only if the abstraction remains honest
