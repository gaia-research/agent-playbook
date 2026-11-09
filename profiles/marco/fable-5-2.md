# Claude Fable 5.2: prompting and migration notes

Status: **adopted operator preference**, 2026-11-10. This is a model-specific
supplement to [Marco's profile](PROFILE.md), not a change to the portable
[PLAYBOOK](../../PLAYBOOK.md), nor a harness configuration.

## Routing decision

Whenever an authorized task would have selected **Claude Fable 5.1**, prefer
**Claude Fable 5.2**. Do **not** replace Opus, Sonnet, Haiku, Flash, Sol, Luna,
Terra, or other models merely because Fable is newer. Fable remains a
higher-cost specialist for ambitious, long-horizon technical work. Honor
existing explicit tier-first routing, planner-effort preferences, budgets,
subagent concurrency, identity constraints, and review/merge/deployment gates.
No automatic escalation to Fable, Mythos, or premium fast mode.

Use Claude API model ID `claude-fable-5-2`; on Amazon Bedrock use
`anthropic.claude-fable-5-2`. These IDs are **provider-documented**, not
evidence that Pi, Antigravity, Claude Code, or the user's account can run them.
Resolve the exact provider/model/effort and effective fallbacks by local preflight.
If the requested route is unavailable, stop that dispatch and seek an explicitly
authorized alternative. Never silently revert to Fable 5.1.

## Prompt design for 5.2

1. **Calibrate effort.** Start an evaluation at explicit `high`; compare
   `medium` and `xhigh` against representative tasks. Use `low` for simple
   work, `max` only where justified. Most model-specific gains arrive by
   `high`, but an explicit authorized planner MAX preference still takes
   precedence when supported. Effort values are not universally portable
   across providers and harnesses.
2. **Finish the authorized task.** Tell the agent to diagnose recoverable
   timeouts, tool errors, and ordinary failures and continue within the
   existing authority and resource budget. Do not present a list of remaining
   work as completion. Stop at deliberate restrictions, safety barriers,
   missing approvals, or true dependencies, and report blockers precisely.
3. **Spell out approvals by action.** Separate reading, editing, pushing,
   opening PRs, merging, deploying, sending external messages, and changing
   credentials. An instruction to persist through ordinary errors does not
   grant new permissions or bypass human approval.
4. **Bound code ownership.** Define owned files and behavior. Ask for
   necessary changes within scope, not blanket ownership of the whole
   codebase. Avoid drive-by refactors, duplicate implementations, and
   unrequested behavior changes. Inspect the diff, not just the recap.
5. **Delegation is optional.** Give the lead discretion not to spawn agents
   for small tasks. For permitted fan-outs, preflight exact agents/models,
   tools, effort, permissions, fallbacks, concurrency and budget; default
   maximum is four. Do not let Fable's eagerness to delegate override the
   adopted roster or independent review.
6. **Communicate during long turns.** Give a short intent statement and
   occasional concrete progress updates. Some API clients omit Fable's
   thinking-block progress by default; check client rendering before adding
   noisy reminders. Preserve the playbook's exact four-line *final* GitHub
   receipt, and put detailed findings/validation in the committed handoff.
7. **Audit inherited prompt clutter.** Remove obsolete duplicated
   instructions only when authorized and evidence supports doing so.
   Test old assumptions about subagents, “think less” wording, token-budget
   text, verbosity limits, and prohibitions that accumulated without a
   remaining rationale. Never strip security, scope, or approval controls
   as a shortcut.

## API and harness migration checklist

- Confirm model ID and access. Fable 5.2 requires **30-day data retention** on
  the Claude API unless Anthropic expressly authorizes an exception; check
  environment policy before moving traffic. Treat pricing and quotas as live
  facts, not immutable profile data.
- Adaptive thinking is always enabled. Do not send manual thinking budgets,
  `thinking: {type: "disabled"}`, assistant prefills, or unsupported sampling
  parameters `temperature`, `top_p`, and `top_k`. Forced tool selection
  (`tool_choice` of `any` or a named `tool`) is unsupported.
- Preserve prior thinking blocks unchanged, including empty ones, and keep
  conversation history append-only. Fable 5.2 applies prefix validation to
  every account; changing earlier system instructions, tool declarations, or
  messages can trigger a 400 error. Apply fresh prompt changes to **new
  conversations**; mid-conversation changes belong in a new turn or an
  explicitly supported append-only mechanism.
- If custom code manages the agent loop, verify the current computer-use
  toolset, model switching, and advisor restrictions. A Fable 5.2 executor's
  Anthropic advisor must be Fable 5.2 or Mythos 5.2 when using that API
  feature; this does **not** mean all Gaia advisor roles must be Fable.
  Re-check integration support rather than assuming older tools work.
- Run representative smoke tests and an effort/cost sweep **before**
  changing live harness defaults. Distinguish inspected documentation,
  validated static configuration, and a successful authenticated runtime
  dispatch. Refusal/safeguard responses do not authorize covert fallback or
  bypass of controls.

## Provider references (checked 2026-11-10)

- [Official model overview](https://platform.claude.com/docs/en/models/fable-5-2/overview)
- [Prompting Claude Fable 5.2](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-fable-5-2)
- [Claude Fable 5.2 migration guide](https://platform.claude.com/docs/en/models/fable-5-2/migration-guide)

This document records a selection preference and research-backed guidance.
It does not install a model, change runtime settings, permit a fallback,
or guarantee provider availability.
