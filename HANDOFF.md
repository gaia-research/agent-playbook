# Agent Playbook delivery handoff

Status: READY FOR REVIEW. Prepared 2026-11-08. Delivery scope is documentation and
a public feature-branch PR, not installation, provider certification, or deployment.

## Implementation and decisions

Preserved original scaffold commit `42a61e4561997e6022ca7945ac83d0d7d6b4d129` in
history. Reconciled it with the explicit “Recover and Publish Agent Playbook” memory
bridge. Cloud-memory access is not a dependency. No private history or credentials
were copied. The newer instruction supersedes the original four-skill proposal:
only orchestrate and prompting remain; handoff and independent review are canonical
PLAYBOOK conventions. MEMORY is the standalone conversational ingestion entry.
Marco's dated profile and minimal YAML carry personal preferences; the template
lets others replace those choices without changing either skill. MIT licensed.

The memory bridge establishes four-agent default concurrency, MAX/HIGH planning,
cost per verified successful outcome, fail-closed specialist identity, and role
preferences. Actual provider availability remains a local preflight fact. No runtime,
mandatory package/CI, CLI, submodule, or duplicated pi-config implementation exists.

## Sources and compatibility findings

- Current recovery brief: authoritative personal preferences and two-skill scope.
- pi-config committed snapshot `176a5956b7c35775b204e4bdb9e432521f33d730`:
  agent frontmatter, settings/subagent templates, optional-package list, and subagent
  guide. Used `git show HEAD:...` for model candidates to avoid dirty overrides.
  Unrelated modified agent/test files were left untouched.
- Installed package metadata/read-only source: `@parke.dev/pi-subagent` 0.8.0 and
  `pi-antigravity` 0.12.0. README/schema document plan mode; policy and orchestrator
  show retry/fallback resolution. Empty fallback arrays inherit defaults, so they
  must not be presented as a way to disable fallback. Zero retries also leaves
  fallback attempts enabled when the resolved list is nonempty. No child was launched.
- Official Claude, Codex, Pi skill docs and DeepSeek model-list documentation were
  read online. Links and installation locations appear in
  [harnesses.md](profiles/marco/harnesses.md). No live skill installation was tested.

Historical worker-flash/scout-flash/scout-lite aliases are absent. Existing exact
candidates are listed separately from preference labels. Opus planner's configured
HIGH differs from MAX-first preference; preflight must resolve support before an
override. Haiku has no verified concrete mapping. Worker/planner identities are not
automatically read-only reviewers. Agy's observed planner persona is an Antigravity
provider path, not proof of an ACP integration. Model IDs are source-observed, not
certified currently available through provider accounts. These are explicit local
setup/preflight limitations, not blockers to publishing a portable playbook.

## Validation and walkthroughs

Documentation/structural checks, not real fresh-session or authenticated model tests:

1. ChatGPT: followed README → MEMORY → PLAYBOOK/profile. MEMORY is self-contained,
   separates universal defaults from opt-in personal preferences, reconciles existing
   memory, and describes context-only use when persistence is unavailable. A memory
   request explicitly grants no installation/execution/deployment authority.
2. Pi: followed README → orchestrate → profile/harness notes. An existing setup can
   resolve candidates, inspect plan mode, check effective identity/permissions/effort
   and failover, and stop on mismatches. Installation requires consent. An empty
   fallback list must not be assumed to disable inherited configuration.
3. Claude/Codex: followed README → prompting → PLAYBOOK delivery/review. Intent-first
   prompts and the exact four-line receipt require no Pi dependency. Official skill
   locations are linked; the install procedure preserves collisions and requires
   verifying discovery after authorized copying.

Static checks resolve local Markdown links, require exactly two skills with matching
frontmatter, parse both YAML files, check roster aliases and concurrency, reject
removed-skill references, verify the receipt, and scan tracked content for private
paths/token patterns. Whitespace is checked with `git diff --check`.
Results: PASS — 22 local Markdown links; exactly two matching skill headers;
exact receipt; no stale removed-skill references or private-pattern matches.
Both YAML documents parsed with the existing local `yaml` library (no dependency
added): eight model preferences, six role mappings, and concurrency four.
`git diff --check` passed. These are structural results, not provider tests.

## Git delivery

The public repository is `gaia-research/agent-playbook`. Main has a license-only
bootstrap baseline. The feature branch retains the original scaffold history and
incorporates that baseline, establishing a common ancestor without putting the
implementation onto main. The final receipt identifies pushed HEAD. Verify the
report at that head and review `main...HEAD`; do not merge or deploy.

## Outstanding issues

No publication-scope blocker. Provider availability, native installed skill discovery,
real model execution, unsupported historical aliases, and any separate Agy ACP
integration require task-local verification before use. No promise of automatic
memory synchronization or universally supported model/effort mappings is made.
