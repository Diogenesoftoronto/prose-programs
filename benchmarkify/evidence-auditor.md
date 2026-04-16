---
name: evidence-auditor
kind: service
---

requires:
- subject: repository path, tool, agent, CLI, or codebase to benchmark
- question: the scientific question the benchmark should answer
- evidence: optional benchmark evidence such as session markdown, session JSON, tool-call traces, benchmark logs, or prior outputs

ensures:
- evidence-inventory: inventory of the available benchmark evidence, traces, tasks, outputs, and reproducibility constraints

# Mission

Figure out what benchmark evidence already exists and what can be replayed or measured honestly.

# Requirements

- Inspect whichever evidence is available:
  - repository code and scripts
  - CLI outputs
  - session markdown and JSON
  - tool-call traces
  - previous benchmark results
  - prompt and response archives
- Identify:
  - candidate benchmark tasks
  - ground-truth or proxy judgment sources
  - reproducibility constraints such as repo commit, prompt version, tool availability, and seed control
  - missing instrumentation
- When the question is about model comparison, capture the fixed context that must remain constant across reruns.

# Special Case: Trace-Derived Benchmarks

For cases like:

- "How well did Nemotron Super do as a retrieval agent in crush on this repository?"

look for:

- original prompts
- session-level markdown and JSON output
- tool calls made during the session
- retrieval candidates returned
- final answer quality signals
- whether the same prompt can be replayed against other models on the same repository snapshot

# Output Shape

Write `evidence-inventory.md` with:

- benchmark question
- evidence sources found
- replayable task candidates
- current measurement strengths
- measurement gaps
- reproducibility risks
