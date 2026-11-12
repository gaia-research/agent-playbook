# Gemini 4 Hydrogen: prompting and Pi migration

Status: **operator-adopted Gemini Flash successor, 2026-11-13**. Hydrogen replaces **Gemini 3.8 Flash** now in Gaia Gemini Flash roles. **DeepSeek V4.1 Flash remains a separate reserve Flash agent**, never an automatic fallback. This is a personal model-profile decision, not an update to Pi runtime or a replacement for other model tiers.

## Route, effort and authority

Google's documented API model ID is `gemini-4-hydrogen`. For Gaia use **LOW** for scouts, **MEDIUM** for bounded routine workers, **HIGH** for leads and complex implementation. **XHIGH** is available but requires an explicit justification, suitable local support and authorization, not a blanket upgrade. Google's API defaults to HIGH; explicitly select workload-appropriate effort. Keep tier-first cost routing, no silent fallback, no automatic escalation, 4 maximum concurrent subagents by default, independent reviewers, and separate permissions for preview, pushing, merge and production. Retain the distinct cheaper `scout-lite` identity.

Google reports higher agentic coding and tool-use performance and fewer fabricated claims than 3.8 Flash. These are provider results, not Gaia validation. Begin using the authorized replacement after local capability preflight; measure cost per verified result and collect actual successes, retries and failures without delaying the adoption for a comparative benchmark.

## Prompting pattern for Gaia

**Mission → authoritative inputs → owned scope → constraints/permissions → execution and delegation → observable definition of done → evidence and handoff.** Keep prompts compact, avoid duplicated policy boilerplate and let capable agents choose bounded implementation details. Scouts (LOW): inspect the named context and return grounded references, unknowns and a recommendation. Workers (MEDIUM): make surgical changes, run specified tests, state precisely what passed, and deliver a pushed branch and handoff if GitHub delivery is authorized. Leads (HIGH): coordinate independent owned tasks and integration, choose delegation only when useful, preflight the roster and budget, maintain an independent reviewer, and verify the result. Do not mistake greater capability for architectural or approval authority. Recover from ordinary errors within approved budgets, but stop at missing permissions or hard blockers. Never invent test/tool evidence. Use the established four-line PR/Commit/Handoff/Status receipt.

## Google API differences and transport

- Official Google model ID: `gemini-4-hydrogen`. **Pi or Antigravity provider availability and exact routing syntax are not verified by the Google API model listing.**
- Native Google APIs use `thinking_level` values `LOW`, `MEDIUM`, `HIGH`, `XHIGH`. Retire `thinking_budget` and `MINIMAL`. Validate Pi's own effort spelling and mapping, especially older `:minimal` aliases.
- Remove ignored/unsupported explicit `temperature`, `top_p`, `top_k` and manually referenced `cached_content` when migrating supported API calls.
- In custom agent loops preserve `thought_signature` in previous turns, including tool calls and final text. In parallel tool-call turns retain it only on the first function-call part. With history editing or compaction use `prefix_mismatch_behavior="DROP"` when supported. Verify the Pi adapter really supports these semantics; do not patch tool signatures blindly.
- Google's 1,048,576-token context is **unified across input and output**, including thinking and tool calls. Foreground generations have a 65,536-token per-segment maximum. Longer decodes need compatible continuation support. Google's Interactions SDK automatic continuation requires Python `google-genai >= 2.34.0` or JS `@google/genai >= 2.32.0`; this does not establish Pi compatibility.

## Pi-config procedure

1. Inspect the installed Pi version, providers, model catalog (`/model`), authentication and actual supported effort settings; use the **real resolved** Hydrogen route. If the model is not listed and there is no verified compatible provider, **stop without changing routing**.
2. Read current pi-config and `~/.pi/agent/models.json`, avoiding overwrites of other models or credentials. A custom model is an option only with a proven supported transport, not an invented `antigravity/gemini-4-hydrogen` identifier.
3. Migrate only prior Gemini Flash usages: lead, generic `worker` (alias `worker-flash`), generic `scout` (alias `scout-flash`), and related explicitly mapped Gemini routes. Map scout LOW, worker MEDIUM, lead HIGH with the harness's supported syntax. Preserve DeepSeek V4.1 Flash as a reserve, `scout-lite`, and all non-Gemini specialists.
4. Use `@parke.dev/pi-subagent` `action:"plan"` when supported, to inspect effective agent/model/effort/profile/tools/permissions/isolation/budget/concurrency/**fallbacks**. In older versions, empty `fallback_models` can inherit defaults, so verify effective routing instead of assuming fallback disabled.
5. Smoke-test an authenticated read-only scout, a bounded worker tool call and multi-turn tool/signature handling. Record what was actually tested. No implicit extension installation, paid-provider activation, key changes, merges or deployments.

## References checked 2026-11-13

- [Google Gemini 4 migration](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/start/get-started-with-gemini-4)
- [Google Hydrogen developer guide](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/guides/gemini-4-hydrogen)
- [Google Hydrogen model card](https://deepmind.google/models/model-cards/gemini-4-hydrogen/)
- [Pi custom model docs](https://github.com/badlogic/pi-mono/blob/main/packages/coding-agent/docs/models.md)

This document does not change native Pi configuration or prove that Hydrogen is available in the operator's Pi/Antigravity session.
