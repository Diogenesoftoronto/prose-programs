---
name: composify
kind: program
services: [prose-reader, composition-planner, variant-composer, composition-writer]
---

requires:
- documents: two or more OpenProse documents, program paths, or pasted document contents to compose
- variants: number of composition options to generate (default: 3)
- goal: what the composed document should accomplish
- composition-style: preferred composition mode such as "pipeline", "parallel", "worker-critic", "captain", "minimal", or "mixed" (optional)

ensures:
- inventory: inventory of the source documents, their contracts, and reusable pieces
- composition-options: multiple viable ways to compose the source documents
- composed-documents: composed OpenProse document variants that satisfy the requested goal
- report: recommendation explaining which composition to use and why

strategies:
- when documents overlap heavily: merge contracts instead of nesting redundant services
- when documents conflict: isolate incompatible assumptions and propose distinct variants
- when the requested number of variants is high: vary control style, decomposition depth, and failure handling
