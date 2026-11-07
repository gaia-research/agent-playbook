# Cloud-agent handoff

Status: BLOCKED — complete local scaffold; cloud-memory extraction and GitHub
publication remain outstanding. Prepared 2026-11-08.

## Scope and architecture

The operator explicitly requested scaffolding only if cloud memory was unavailable.
No cloud conversation-memory read capability was exposed in this session. Local
memory is not a substitute. No cloud history was extracted or persistent memory
written. No repository was published, PR opened, or branch pushed.

README routes two independent paths: MEMORY is a self-contained conversational
entry; PLAYBOOK is canonical portable policy; four standalone skills implement
procedures. Marco's profile is separate and incomplete; the template and examples
allow others to adapt the core. YAML is non-native declarative data. MIT license.
No runtime, CLI, package manager, required dependencies, or installations.

## Sources and reconciliation

- Operator-supplied “Astra: Scaffold Gaia Agent Playbook” brief: architecture,
  four skills, delivery format, consent boundaries, and quality criteria.
- Current operator instructions: subagent naming labels and fully specified custom
  task names. No mapping of those display labels to provider model IDs is inferred.
- Local pi-config read-only snapshot at abbreviated HEAD `176a595`: README.md,
  subagent.json.template, and docs/subagent-thinking-levels.md. The working tree
  had modified agent/test files; these were not used to extract roster truth.
- Available tool inventory: no cloud conversation-memory reader. A local memory
  registry keyword search yielded no relevant Agent Playbook/cloud-memory entry.

Conflict requiring cloud reconciliation: pi-config's template configures fallback
models; the brief requires no silent fallback. The scaffold preserves the brief's
rule and requires inspection of effective runtime behavior before dispatch. It
neither rewrites pi-config nor adopts those template routes as personal policy.

Current provider model IDs, capabilities, native config syntax, AGY integration
identity, historical role patterns, and fallback/escalation preferences have not
been verified. Empty roster entries mean unresolved. The personal profile is not
ready for plug-and-play use. Public compatibility claims must wait for official
provider/harness documentation and canonical configuration checks.

## Validation evidence

Static documentation validation, not live harness or fresh-model execution:

1. Fresh ChatGPT walkthrough: README → MEMORY → PLAYBOOK works without skills.
   MEMORY distinguishes stable preferences from transient roster facts, requires
   personal-profile consent, reconciles existing memory, and explicitly describes
   context-only operation when persistence is unavailable. Expected result: useful
   context, no unsupported claim that memory was saved.
2. Fresh Pi walkthrough: README selects individual skills; harness notes require
   version/schema/roster/fallback checks and consent before copying anything.
   Empty model assignments prevent a claim of ready-to-run dispatch. Expected
   result: bounded installation proposal; setup and real discovery remain untested.
3. Fresh Codex/Claude walkthrough: Markdown procedures work as context without Pi;
   installation is conditional on each target's verified discovery/security model.
   Expected result: portable intent and evidence rules, no assumed native adapter.

A Python static check resolves all relative Markdown links, requires four skill
frontmatter names/descriptions, checks unresolved YAML markers, and checks the
four-line handoff template. `git diff --cached --check` verifies whitespace.
Result: PASS — 22 relative links, 4 skill headers, 2 pending-profile markers,
and exact receipt. Staged whitespace check passed.

No live installations, provider requests, test agents, deployment, or memory writes
were performed. These walkthroughs demonstrate document paths, not compatibility.

## Cloud agent continuation

1. Read the supplied brief and this scaffold. Obtain cloud history through the
   available supported mechanism; do not claim access from a summary alone.
2. Extract established personal decisions with public-safe provenance and rationale.
   Resolve newer/current instructions against older choices; keep project-specific
   decisions out of universal policy. Populate the profile and YAML only after
   verifying concrete IDs, supported efforts, and integration syntax. Resolve
   fallback conflicts explicitly, and leave any remaining unknowns labeled.
3. Verify official Claude/Codex/Pi/DeepSeek documentation and canonical repositories
   read-only. Add only thin optional declarative setup guidance; do not install
   anything without explicit consent. Repeat the three walkthroughs.
4. Review all public content for private details. Under the brief's publishing
   authorization, create `gaia-research/agent-playbook` publicly if permitted.
   Establish an appropriate base branch, push this feature work, and open a PR.
   Do not merge. Update this report with actual validation and remaining issues.
5. Verify pushed HEAD and report, then return the brief's exact four-line receipt.

The local repository is isolated from an unrelated parent Git repository. Use this
folder's own Git root, never its parent. Existing local graft cache is ignored.
