---
name: migratify
kind: program
services: [source-auditor, target-mapper, migration-planner, migration-writer]
---

requires:
- project: repository path, project directory, or project brief to migrate
- target-stack: target language, framework, runtime, or toolchain
- migration-goal: what success means, such as performance, portability, hiring, runtime simplification, or ecosystem fit
- migration-style: "incremental", "big-bang", or "hybrid" (default: "incremental")

ensures:
- inventory: inventory of the current project's architecture, tooling, and migration-sensitive constraints
- mapping: source-to-target capability map showing how the current system translates to the target stack
- migration-plan: phased migration plan with risks, compatibility seams, and cutover strategy
- report: migration report with recommended path, non-goals, and first implementation milestones

strategies:
- when migration should not happen: say so clearly and explain why
- when partial migration is safer than full replacement: isolate seams and recommend a hybrid route
- when ecosystem gaps exist in the target stack: call them out early instead of hand-waving adapters
