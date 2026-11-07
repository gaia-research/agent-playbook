# Harness setup and compatibility

Checked 2026-11-08. Documentation and source inspection are distinct from runtime
verification. No integrations, skills, hooks, credentials, or provider requests
were installed or changed. The YAML here is profile data, not native harness config.

## Install only after consent

1. Select `orchestrate`, `prompting`, or both, and choose user or project scope.
2. Read the target's current documentation and local security policy. Inspect
   existing destination files and show a concrete copy plan; preserve collisions.
3. Obtain explicit consent, then copy each chosen `skills/<name>/` directory intact
   to the supported discovery location below. No additional packages are required.
4. Provide the agent with PLAYBOOK.md (from this checkout or its public repository
   URL) and the explicitly adopted profile as context. Keep canonical policies in
   those documents rather than duplicating them inside installed skills.
5. Verify discovery/invocation in that harness. Roll back only the files installed
   by this operation if discovery fails. Do not overwrite unrelated configuration.

| Harness | Documented local discovery | Evidence and limits |
| --- | --- | --- |
| Claude Code | `.claude/skills/<name>/SKILL.md` or `~/.claude/skills/<name>/SKILL.md` | [Official skills documentation](https://code.claude.com/docs/en/skills); managed policies and cloud sessions differ. |
| Codex | `.agents/skills/<name>/SKILL.md` or `~/.agents/skills/<name>/SKILL.md` | [Official skills documentation](https://learn.chatgpt.com/docs/build-skills); discovery is subject to local configuration. |
| Pi | `.agents/skills/<name>/SKILL.md` or `~/.agents/skills/<name>/SKILL.md` | [Official skills documentation](https://pi.dev/docs/latest/skills); inspect version and configured paths. |

For conversation-only use, read the documents directly. No installation is needed.

## Pi dispatch preflight

Installed package metadata was inspected read-only: `@parke.dev/pi-subagent` 0.8.0
and `pi-antigravity` 0.12.0. The former's installed README documents `action:
"plan"`, as does the [upstream README](https://github.com/LukasParke/pi-subagent).
The installed package identifies its current source as
[LukasParke/pi-extensions](https://github.com/LukasParke/pi-extensions/tree/main/packages/pi-subagent).
This does not prove an extension is loaded in a particular session.

For an already configured environment, resolve the selected agent first. A plan
request uses the installed tool's schema, with an explicit task, agent, model,
effort, profile, tools, permissions, budget, isolation, and no unapproved fallback.
Inspect the returned resolution before dispatch. Do not paste placeholder model IDs
into a launch request. Plan mode validates a request; it does not prove a provider
call will succeed. If plan is unsupported, perform equivalent read-only checks and
report that limitation rather than invoking guessed syntax.

The source-observed candidate mappings in models.yaml come from pi-config commit
`176a5956b7c35775b204e4bdb9e432521f33d730` using committed agent files, not dirty local
overrides. Standalone `worker-flash`, `scout-flash`, and `scout-lite` files are absent here,
but the operator confirms `worker-flash` → `worker` and `scout-flash` → `scout`.
Committed `worker.md` selects `antigravity/gemini-3.8-flash:medium`; `scout.md`
selects `antigravity/gemini-3.8-flash:minimal`. Both targets were checked read-only.
Resolve those generic agent definitions rather than requiring alias-named files.
`scout-lite` remains an environment-specific cheaper Gemini Lite option; the
operator has it in another environment and retains it for future Lite releases.
`worker-flash-medium` is a candidate, never an automatic alias replacement.
`planner-opus` pins HIGH; the operator's MAX-first preference requires checking
support and the exact override syntax. Shared Sol/Terra variants have mixed effort
fields and alternate providers; do not copy them as equivalent billing routes.
Luna/Terra preferences for review do not make worker/planner agent permissions
suitable for review: explicitly select a read-only review profile and inspect tools.
Haiku is an established preference with no resolved mapping in the inspected roster.

pi-config's subagent template supplies fallback models. That configuration conflicts
with an unapproved failover policy: before dispatch, verify that effective fallback
and retry behavior cannot substitute identities. If this cannot be guaranteed, stop
that dispatch and request a bounded explicit choice. In inspected version 0.8.0,
`src/policy.ts` treats an empty `fallback_models` array as inheritance, not disabling
fallbacks. Even `max_retries: 0` does not disable nonempty resolved fallbacks: the
orchestrator uses `1 + max(maxRetries, fallbacks.length)` attempts. Require a plan
with no effective fallback routes and zero retries, using an already approved
configuration, or block specialist dispatch pending a separately authorized fix. Do not edit global config as
an implicit repair. Concurrency defaults to four for this profile, regardless of
larger runtime ceilings. A failed preflight is not permission to switch credentials.

## Agy, Antigravity, and DeepSeek

The committed `planner-agy` definition routes to
`antigravity/gemini-3.1-pro:high`; pi-config's package template names `pi-antigravity`.
This is evidence of a Pi provider/persona path, not proof of a separate ACP bridge.
No separate Agy/Antigravity ACP subagent integration was verified. An explicit ACP
request must fail closed until its installed implementation and syntax are checked.
Do not conflate the historical Agy persona with newer Argon escalation routes.

DeepSeek is an operator-authorized provider option; `deepseek/deepseek-flash:high`
is a source-observed candidate, not a guarantee of account access or model support.
Use the provider's [model-list API documentation](https://api-docs.deepseek.com/api/list-models/)
to check current IDs and effort/capability metadata through the configured harness.
Keep secrets in that harness's existing credential mechanism. Provider access does
not imply permission to change credentials, purchase credits, or select paid fallback.

Agent Playbook owns portable policy and personal preferences. pi-config independently
owns its runtime, installers, extensions, and native setup. It is optional reference
evidence, never a dependency; do not copy its runtime or run its installers here.
