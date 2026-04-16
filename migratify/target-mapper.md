---
name: target-mapper
kind: service
---

requires:
- inventory: inventory of the current project's architecture, tooling, critical constraints, and migration-sensitive components
- target-stack: target language, framework, runtime, or toolchain
- migration-goal: what success means

ensures:
- mapping: source-to-target capability map with substitutions, gaps, and compatibility notes

# Mission

Map the source system to the target stack honestly.

# Requirements

- For each major capability in the source project, specify:
  - direct equivalent in the target stack
  - adapter or bridge needed
  - unsupported or risky area
- Cover:
  - UI or rendering model
  - state management
  - server or runtime model
  - data access
  - build and packaging
  - testing and release flow

# Output Shape

Write `mapping.md` with a capability-by-capability migration map.
