# Gemini 4 Hydrogen migration handoff (2026-11-13)

## Implementation
- Added `profiles/marco/gemini-4-hydrogen.md`: operator-adopted routing, Gaia prompting, Google API changes, Pi compatibility preflight, signature and context handling.
- Updated Marco profile, declarative models/roster, Pi harness compatibility notes, and README entry point.
- Replaced the **preferred** Gemini 3.8 Flash route with Gemini 4 Hydrogen; retained historically inspected 3.8 Flash source targets as evidence (not current desired dispatch targets).
- Kept DeepSeek V4.1 Flash as separately selected reserve. No changes to general review, approvals, budget/escalation rules, or maximum concurrency.

## Validation evidence
- Read the previous versions of all edited files through GitHub, preserving policy boundaries and original source-observed model configuration.
- Cross-checked Google's Nov 12, 2026 Hydrogen model and Gemini 4 migration docs: official API ID `gemini-4-hydrogen`, LOW/MEDIUM/HIGH/XHIGH, shared context window, signature requirements.
- Documentation-only changes: no runtime tests, authenticated Pi call, provider enumeration, or live subagent execution performed. Thus **Pi/Antigravity Hydrogen availability is unverified**. Source-observed old `:minimal` effort is not presumed to map directly to LOW.
- GitHub patch review and external independent review remain pending on the PR.

## Findings and open items
- Operator explicitly adopted Hydrogen in Gemini Flash roles now, without requiring a prior benchmark.
- Google API availability is not proof of availability through local Pi or Antigravity. Runtime config lives in `mbtiongson1/pi-config`, not this repository.
- A local Pi agent should inspect the model catalog and installed Pi/subagent plugin before attempting to migrate its provider route. Preserve credentials and unrelated model aliases.
- Inspect effective inherited fallback chains: empty fallback list alone may not disable fallback in older `@parke.dev/pi-subagent`.
- Verify tool-thought signatures and conversation compaction semantics in actual transport, then smoke-test.

## Outstanding
- Local Pi preflight and pi-config migration: **not performed**, pending operator-side execution.
- Independent review: pending.
- Merge/deploy: **not authorized**.
