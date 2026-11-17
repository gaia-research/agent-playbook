# GPT-6.2 Astra and Sol: checkpoint succession and prompting

Operator decision: 2026-11-18. This is a **global identity substitution within the same named model families**, not an optional evaluation campaign:

- `gpt-6.1-sol` → `gpt-6.2-sol`
- `gpt-6-astra` → `gpt-6.2-astra`

Apply to current/future playbook routing and prompts where these exact families are requested. Preserve historical evidence, archived handoffs, unrelated Luna/Terra/Anthropic/Gemini models, and explicit scope/permissions. If a configured environment does not expose the new checkpoint, fail closed and report that preflight failed: **no automatic fallback to the older model**. This repository is documentation, not the runtime harness configuration.

## Official sources

- [Using GPT-6.2](https://developers.openai.com/api/docs/guides/latest-model?model=gpt-6.2-astra)
- [GPT-6.2 release](https://openai.com/index/introducing-gpt-6-2-astra-sol/)
- [Reasoning models](https://developers.openai.com/api/docs/guides/reasoning)

## Prompt and API migration notes

- Astra is more concise by default; remove redundant blanket brevity demands where they impair evidence and handoffs. Final user-facing artifacts should be self-contained and appropriate to the intended audience.
- For authorized long tasks, specify the observable outcome, permit reasonable reversible assumptions, and encourage continuation to validation rather than stopping to propose an obvious next step. This does **not** grant merge, deployment, destructive-action or escalation authority.
- Describe repository coding conventions, compatibility constraints, and relevant visual/typographic references for UI work; reuse existing logic and check outcomes. Avoid unnecessary abstractions and ceremonial tests.
- For new API integrations, begin at reasoning effort `medium`, then measure and tune for task complexity; existing explicit effort selections are **not** silently overridden. `none` and `minimal` migrate to `low` for GPT-6.2. Supported effort must be confirmed in the actual harness.
- GPT-6.2 tool calling requires the **Responses API**, even though ordinary text requests support Chat Completions. Remove unsupported sampling/logprob parameters when migrating API requests, as detailed in the official guide.
- Preserve stable conversation prefixes and append fresh instructions. Mid-conversation prefix edits, model downgrades or identity/organization changes can invalidate preserved reasoning items; handle history and caching per API guidance.
- Distinguish provider-announced availability from actual local harness/account/provider route. Do not silently change provider, model, effort, credentials, or billing route.
- Preserve existing Playbook independent-review and four-line delivery receipt. Do not equate checkpoint succession with new authority.

This note is intentionally concise; consult the current official model guide before changing executable API integrations.
