---
name: productize
kind: program
services: [readiness-auditor, packaging-designer, docs-designer, release-writer]
---

requires:
- subject: internal tool, library, research repo, or prototype to productize
- audience: intended users or buyers
- distribution: how the product should be delivered, such as package, SaaS, binary, or internal platform
- productization-style: "minimal", "balanced", or "full" (default: "balanced")

ensures:
- readiness-inventory: readiness audit covering gaps between current state and usable product state
- packaging-plan: product packaging and distribution design
- docs-plan: onboarding, docs, and support surface design
- report: productization plan with release path and constraints

strategies:
- productize the narrowest useful slice first
- prefer shipping a clear product over exposing every internal capability
- do not confuse technical completeness with product readiness
