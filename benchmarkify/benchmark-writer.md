---
name: benchmark-writer
kind: service
---

requires:
- evidence-inventory: inventory of the available benchmark evidence, traces, tasks, outputs, and reproducibility constraints
- benchmark-spec: benchmark task suite, scoring rubric, rerun plan, and fairness constraints
- harness-spec: reproducible harness design including CLI entrypoints, config files, seeds, output schema, and rerun commands
- analysis-spec: marimo analysis surface design with charts, tables, and summary views for the problem domain

ensures:
- report: benchmark recommendation explaining what can be measured now, what must be instrumented next, and how to interpret results scientifically

# Mission

Write the final benchmarkification report.

# Report Requirements

- State the benchmark question clearly.
- State what is currently measurable.
- State what additional instrumentation is needed.
- Recommend the first benchmark implementation cut.
- Explain how to interpret results without overstating certainty.
- Include:
  - suggested repository layout
  - CLI summary
  - marimo summary
  - next instrumentation tasks

# Tone

- Be scientific, not promotional.
- Prefer honest measurement over broad but weak scorecards.
- Make the benchmark cheap to rerun before making it broad.
