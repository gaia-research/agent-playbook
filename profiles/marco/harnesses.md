# Optional harness setup

This scaffold does not verify current provider models or supply native config.
The profile YAML is declarative playbook data only. Core skills are plain Markdown
and can be used as conversation instructions independently of installation.

| Target | Cloud-agent verification before installation |
| --- | --- |
| Claude Code | Current official skill format/discovery, project versus user scope, tool permissions, actual model and effort support. |
| Codex | Current official skill discovery, applicable project instructions, supported model/effort and delegation API. |
| Pi | Installed version, skill discovery, actual roster, provider access, subagent schema and fallback rules. |
| `@parke.dev/pi-subagent` | Exact installed version and supported arguments; isolated child ownership, process limits, effective fallback resolution. |
| AGY / Antigravity | Resolve the intended integration from cloud history, then verify its canonical implementation and supported provider routes. No compatibility claimed. |
| DeepSeek API | Verify official model IDs, endpoint/auth setup and reasoning/tool support for the chosen harness. Keep secrets outside this repository. |

Read-only local evidence: pi-config at abbreviated HEAD `176a595` documents Pi
subagent definitions and a `subagent.json.template` with configured fallback
models. That is source evidence, not live capability verification or authorization
to adopt those fallbacks. Its working tree was dirty; no modified agent files were
used as personal-roster truth. Do not run its README setup commands during review.

Agent Playbook owns intent, authority, evidence standards, and adopted preferences.
pi-config owns its runtime, extensions, installers, and harness-specific policies.
Keep it independent; no submodules, dependency copying, or automatic installers.

After explicit installation consent: inspect the destination, propose selected
skill copies and any thin adapter, preserve collisions, use the target's verified
native format, and verify discovery. Installation consent does not authorize
credential changes, paid fallback routes, or arbitrary hook installation.
