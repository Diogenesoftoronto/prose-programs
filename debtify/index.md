---
name: debtify
kind: program
services: [debt-reader, debt-prioritizer, sequence-designer, debt-writer]
---

requires:
- subject: repository, system, or workflow with technical debt to analyze
- goals: optional business, engineering, or reliability goals
- debt-style: "quick-wins", "balanced", or "structural" (default: "balanced")

ensures:
- debt-inventory: inventory of debt items, sources, and drag
- priority-model: prioritization model with cost, payoff, and risk
- execution-plan: sequenced plan for paying debt down
- report: debt reduction report with rationale and next steps

strategies:
- distinguish debt from preference disputes
- prioritize debt that blocks speed, correctness, or changeability
- avoid debt plans that are really hidden rewrites
