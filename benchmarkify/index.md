---
name: benchmarkify
kind: program
services: [evidence-auditor, task-curator, harness-designer, analysis-designer, benchmark-writer]
---

requires:
- subject: repository path, tool, agent, CLI, or codebase to benchmark
- question: the scientific question the benchmark should answer
- evidence: optional benchmark evidence such as session markdown, session JSON, tool-call traces, benchmark logs, or prior outputs
- benchmark-style: preferred style such as "offline replay", "task suite", "trace audit", "model comparison", or "mixed" (default: "mixed")
- rigor: desired rigor level -- "quick", "standard", or "publication" (default: "standard")

ensures:
- evidence-inventory: inventory of the available benchmark evidence, traces, tasks, outputs, and reproducibility constraints
- benchmark-spec: benchmark task suite, scoring rubric, rerun plan, and fairness constraints
- harness-spec: reproducible harness design including CLI entrypoints, config files, seeds, output schema, and rerun commands
- analysis-spec: marimo analysis surface design with charts, tables, and summary views for the problem domain
- report: benchmark recommendation explaining what can be measured now, what must be instrumented next, and how to interpret results scientifically

strategies:
- when trace evidence exists: prefer replayable task extraction from those traces over invented tasks
- when comparing models: hold prompts, repo snapshot, tools, and evaluation criteria constant
- when the benchmark question is vague: sharpen it into one measurable claim before designing the harness
- when exact judgments are difficult: use structured rubrics, pairwise comparisons, or task-specific metrics instead of vague vibes
- when reproducibility is weak: prioritize frozen datasets, seeded reruns, versioned configs, and stable output schemas before adding more charts
