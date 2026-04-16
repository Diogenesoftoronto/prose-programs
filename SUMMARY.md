# Repository Summary

This repository contains a library of OpenProse programs.

The programs are grouped by job:
- workflow extraction and generalization: `prosify`, `syncify`, `updatify`, `adoptify`
- reduction and modeling: `distillify`, `frameworkify`, `composify`
- creation and packaging: `productize`, `datasetify`, `instrumentify`, `traceify`
- change and repair: `migratify`, `stabilify`, `repairify`, `debtify`
- assessment and governance: `reviewify`, `evalify`, `benchmarkify`, `guardraily`

Each program declares:
- `requires`: the evidence or inputs needed to run it
- `ensures`: the artifacts it should produce
- `strategies`: the decision rules it should follow

The repository is organized as plain Markdown so the program definitions stay readable, reviewable, and easy to version.
