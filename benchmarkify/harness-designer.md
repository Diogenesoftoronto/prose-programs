---
name: harness-designer
kind: service
---

requires:
- evidence-inventory: inventory of the available benchmark evidence, traces, tasks, outputs, and reproducibility constraints
- benchmark-spec: benchmark task suite, scoring rubric, rerun plan, and fairness constraints
- subject: repository path, tool, agent, CLI, or codebase to benchmark

ensures:
- harness-spec: reproducible harness design including CLI entrypoints, config files, seeds, output schema, and rerun commands

# Mission

Design the reproducible execution harness.

# Requirements

- Specify:
  - benchmark dataset layout
  - config schema
  - CLI commands
  - environment variables
  - model matrix
  - seed handling
  - output schema in JSON and markdown
  - raw trace retention
- The harness must be easy to rerun from the command line.
- The harness must freeze the repo or subject state used for each run.
- The harness must make comparisons across reruns mechanically possible.

# Preferred Deliverables

- A simple CLI such as:
  - `benchmarkify run`
  - `benchmarkify compare`
  - `benchmarkify report`
- Versioned benchmark definitions stored in the repository.
- Raw outputs preserved separately from scored summaries.

# Crush-Like Example

For a CLI such as `crush`, include a path for:

- ingesting session markdown and JSON
- extracting prompt plus tool-call traces
- replaying the same task against different models
- scoring retrieval behavior and final answer quality
- comparing cost, latency, and tool use

# Output Shape

Write `harness-spec.md` with:

- file layout
- CLI command design
- config design
- output schema
- rerun instructions
- comparison workflow
