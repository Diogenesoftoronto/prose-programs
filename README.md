# prose-programs

`prose-programs` is a collection of OpenProse programs for turning evidence, repositories, workflows, and failures into reusable prose artifacts.

Each directory is a self-contained program with a small service pipeline and a clear contract:
- `requires`: the inputs the program expects
- `ensures`: the artifacts the program should produce
- `strategies`: the operating rules that shape the output

## Program families

- `prosify`: extract workflows and reusable patterns from evidence.
- `frameworkify`: separate stable primitives from project-specific implementation and package a reusable framework.
- `productize`: turn internal tools or prototypes into shippable products with packaging and docs.
- `distillify`: compress a corpus into core invariants and a reduced mental model.
- `repairify`: analyze failures, identify root causes, and produce fixes with regression guards.
- `reviewify`: read reviews and synthesize findings or patterns.
- `composify`: combine prose assets into new variants or higher-level compositions.
- `datasetify`: derive datasets and labeling/splitting plans from source corpora.
- `instrumentify`: design telemetry, schemas, and instrumentation surfaces.
- `traceify`: normalize traces and design trace schemas and readers.
- `migratify`: plan and execute migrations between source and target systems.
- `stabilify`: reduce instability and design deterministic environments.
- `syncify`: analyze synchronization work and design planner/writer workflows.
- `updatify`: plan upstream merges and repository updates.
- `adoptify`: design adoption and rollout strategies for change.
- `benchmarkify`: design benchmarks, harnesses, and evaluation plans.
- `debtify`: prioritize and sequence debt reduction work.
- `evalify`: design evaluation rubrics, judges, and scoring systems.
- `guardraily`: define policy, risk, and enforcement boundaries.

## Structure

Most programs follow the same shape:

1. A reader or auditor service gathers evidence.
2. A designer or planner service turns that evidence into an actionable model.
3. A writer service produces the final prose artifact.

This repository is intentionally lightweight: the directories contain the program definitions rather than a large application framework.

## Usage

Use the program directory that matches the task:
- Choose `prosify` when you want reusable workflows extracted from real evidence.
- Choose `distillify` when you need a compact mental model of a corpus or codebase.
- Choose `repairify` when something is broken and you need a root-cause and fix plan.
- Choose `frameworkify` or `productize` when the goal is reuse or release readiness.

## Summary documents

- `SUMMARY.md` gives a compact overview of the repository and its program groups.
- The individual `index.md` files define each program contract.
