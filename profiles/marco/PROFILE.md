# Marco's personal profile

Established operator defaults, dated 2026-11-08. Source: the explicit recovery
brief's memory bridge. Adopt only with consent; operator overrides take precedence.
These preferences are configurable, not universal model-ranking claims.
[PLAYBOOK.md](../../PLAYBOOK.md) owns portable policy and GitHub delivery/review.

## Routing and roles

Optimize expected cost per verified successful outcome. Prefer capable lightweight
agents for routine execution and stronger models for architecture, synthesis, and
difficult reviews. Avoid coordination ceremony that costs more than the work.
Use lead, planner, scout, worker, reviewer, and advisor roles with clear ownership.
Default maximum subagent concurrency is **four**, unless explicitly overridden.
Planners prefer **MAX when supported, otherwise HIGH**; other roles use workload-
appropriate effort. Unsupported settings are not permission to silently substitute.

Preferences: Gemini Flash for economical leadership/scouting/routine work; Claude
Haiku for narrow low-cost execution; authorized Claude Opus for difficult planning,
architecture, and synthesis; Sol for architecture-heavy reasoning; Luna and Terra
for verification/review; Argon for designated escalation or independent review;
DeepSeek API as a provider option. Verify access and capabilities at use time.
Codex and Claude are primary coding environments. Pi with `@parke.dev/pi-subagent`
is preferred delegation infrastructure; use Agy/Antigravity within Pi where verified.

Explicitly select provider, model, effort, role, tools, profile, and permissions.
Never silently escalate, substitute models, or change credentials. A named
specialist fails closed if unavailable. Parallelize independent tasks, reconcile
results, and verify actual outcomes. For substantial Pi fan-outs use `action:
"plan"` where supported before dispatch.

## Naming and delivery

When using the operator's Luna/Terra/Sol/Astra naming scheme, display names are
`Model Effort Task`: effort labels Light, Med, High, XHigh, Max, Ultra; tasks Planner,
Worker, Scout, Reviewer, or a fully specified custom task. These labels do not
establish API effort values. For other explicitly requested specialists, preserve
their requested identity and specify the role and actual effort rather than
mislabeling them as one of these four models.

Default GitHub delivery is pushed code, PR, and committed self-contained report.
Use the playbook's exact four-line receipt. Reviewers independently fetch the latest
pushed report from only the PR identifier and handoff path. Never merge without
explicit authorization. Preview, merge, production, and end-to-end authority remain
separate unless the operator explicitly grants a bounded end-to-end workflow.

## Use after local setup

Read [models.yaml](models.yaml), [roster.yaml](roster.yaml), and
[harnesses.md](harnesses.md). They provide preferences and source-observed candidates,
not a native config importer. An already configured agent can apply this profile
as instructions: resolve the desired route, preflight it, report mismatches, and
launch only an exact authorized match. Missing setup fails closed without installing
anything. Do not require pi-config to consume this profile.

Historical aliases and configured mappings have different evidence status. Exact
current capabilities, permissions, and credentials are local preflight facts;
never store them as permanent guarantees. Preserve stable rationale and reconcile
newer decisions without overwriting unrelated memory.
