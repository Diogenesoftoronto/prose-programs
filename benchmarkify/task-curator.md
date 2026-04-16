---
name: task-curator
kind: service
---

requires:
- evidence-inventory: inventory of the available benchmark evidence, traces, tasks, outputs, and reproducibility constraints
- benchmark-style: preferred benchmark style
- rigor: desired rigor level

ensures:
- benchmark-spec: benchmark task suite, scoring rubric, rerun plan, and fairness constraints

# Mission

Turn the evidence into a benchmark that answers the stated question rather than merely producing activity.

# Requirements

- Define the benchmark tasks.
- State what counts as success or failure.
- Choose the scoring method:
  - exact task completion
  - rubric scoring
  - pairwise ranking
  - retrieval precision or recall
  - tool efficiency
  - latency or cost
  - mixed scorecard
- Define fairness constraints so comparisons are valid.
- Specify dataset splits or held-out tasks when the benchmark should resist overfitting.

# Scientific Rules

- A benchmark question must become a measurable claim.
- Do not compare models under different prompts, tools, or repo states unless the benchmark is explicitly about those differences.
- Separate:
  - task quality
  - output quality
  - tool-use quality
  - cost and latency
- When human or model judging is needed, define the rubric precisely enough that different evaluators can follow it.

# Output Shape

Write `benchmark-spec.md` with:

- benchmark question restated as a measurable claim
- task suite
- scoring rubric
- success metrics
- fairness constraints
- holdout or replay strategy
