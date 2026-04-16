---
name: distillify
kind: program
services: [corpus-reader, invariant-extractor, core-model-designer, distillation-writer]
---

requires:
- subject: codebase, repository, document corpus, or workflow corpus to distill
- audience: who the distillation is for
- distillation-goal: what must become easier to understand or operate
- style: "operator", "architect", "newcomer", or "mixed" (default: "mixed")

ensures:
- corpus-inventory: inventory of source material and dominant concepts
- invariant-set: extracted invariants, recurring structures, and non-negotiable facts
- core-model: reduced mental model, command set, and architecture core
- report: distillation report and reusable condensed artifact plan

strategies:
- compress around invariants and commands, not prose summaries
- preserve what is load-bearing, delete ornament
- tailor the distillation to the audience's decisions
