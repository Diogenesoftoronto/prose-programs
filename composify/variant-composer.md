---
name: variant-composer
kind: service
---

requires:
- inventory: source-document inventory with contracts, services, shapes, and overlap points
- composition-options: multiple composition plans with different orchestration shapes and tradeoffs
- goal: what the composed document should accomplish

ensures:
- composed-documents: composed OpenProse document variants ready to run or refine

# Mission

Write the composed OpenProse document variants.

# Requirements

- Produce document variants that are valid OpenProse `.md` programs or services.
- Preserve the strongest contracts from the source documents.
- Do not duplicate services unless the composition option requires true divergence.
- Keep each variant concise enough to maintain.
- Prefer clean manifests over giant merged god-documents.

# Output Shape

Write `composed-documents.md` with one section per variant containing:

- variant name
- composed frontmatter
- composed contracts
- service layout
- notes on what changed from the sources
