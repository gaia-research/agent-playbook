# Handoff: GPT-6.2 checkpoint succession (2026-11-18)

## Implementation
- Upgraded operator-selected Sol from `gpt-6.1-sol` to `gpt-6.2-sol` and introduced explicit Astra alias `gpt-6.2-astra` superseding `gpt-6-astra`.
- Updated profile, prompting skill and README to point at the new migration note.
- Added source-linked model-specific guidance, API constraints, reasoning, tool calling and history-prefix notes.
- No runtime harness config, permissions, unrelated model families, merge or deployment changed.

## Validation evidence
- Checked the repository's current model layer, roster, profile, prompting skill and portable policy before edits.
- Cross-checked model identifiers and migration behavior against official OpenAI GPT-6.2 documentation released November 17, 2026.
- Changes are documentation and declarative profile data only; no executable tests available or run.
- New model availability has NOT been verified in Pi, Codex, Claude, Antigravity, or other connected harnesses.

## Findings / remaining
- Historical source snapshots and older archived handoffs retain old model versions as evidence; they are not active launch targets.
- A separate scoped runtime config migration is needed wherever old IDs are hard-coded outside this repository.
- Independent review and founder merge authorization are still required.
