---
name: analysis-designer
kind: service
---

requires:
- benchmark-spec: benchmark task suite, scoring rubric, rerun plan, and fairness constraints
- harness-spec: reproducible harness design including CLI entrypoints, config files, seeds, output schema, and rerun commands
- rigor: desired rigor level

ensures:
- analysis-spec: marimo analysis surface design with charts, tables, and summary views for the problem domain

# Mission

Design the marimo analysis layer so benchmark results are inspectable and easy to understand.

# Requirements

- Use marimo as the primary analysis surface.
- Specify:
  - required input files
  - summary tables
  - charts and graphs
  - filtering controls
  - per-run drill-down views
  - export surfaces for markdown or static reports
- Choose visualizations that fit the domain.

# Recommended Views

- overall score comparison by model or variant
- retrieval quality by task type
- tool-call counts and tool efficiency
- cost versus quality
- latency versus quality
- run distribution or variance plots
- failure taxonomy counts
- task-level inspection table with links to raw traces

# Output Shape

Write `analysis-spec.md` with:

- marimo notebook structure
- chart plan
- input schema assumptions
- derived metrics
- export and reporting plan
