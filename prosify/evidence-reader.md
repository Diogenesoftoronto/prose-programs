---
name: evidence-reader
kind: service
---

requires:
- source: repository path, git history, conversation log, prompt/result archive, or combined evidence source to analyze
- focus: optional area to mine

ensures:
- evidence-inventory: inventory of observed work, prompts, outputs, decisions, artifacts, and recurring sequences

# Mission

Collect the highest-signal evidence for how work is actually being done.

# Requirements

- Read from whichever evidence exists:
  - repository layout and scripts
  - commit history and commit messages
  - issue or PR artifacts
  - prompt logs
  - conversation transcripts
  - generated outputs and follow-up edits
- Prefer direct evidence of:
  - the prompt or request
  - the actions taken
  - the resulting artifact
  - any revision or critique loop
- Identify repeated sequences, not isolated anecdotes.
- Record missing evidence explicitly.

# Output Shape

Write `evidence-inventory.md` with:

- evidence sources examined
- repeated work sequences
- recurring prompts and intents
- recurring artifacts and outputs
- confidence notes
