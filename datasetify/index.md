---
name: datasetify
kind: program
services: [corpus-reader, label-designer, split-designer, dataset-writer]
---

requires:
- source: sessions, prompts, issues, traces, documents, or repo tasks to turn into a dataset
- target-use: benchmark, training, eval, or analysis use
- labeling-style: "manual", "heuristic", "model-assisted", or "mixed" (default: "mixed")

ensures:
- corpus-inventory: inventory of source examples and quality risks
- label-plan: label schema, quality checks, and annotation rules
- split-plan: dataset splits, holdouts, and leakage controls
- report: dataset design report with generation and maintenance plan

strategies:
- prevent leakage between train, dev, and test
- preserve provenance to the original source
- prefer smaller high-quality datasets over large messy corpora
