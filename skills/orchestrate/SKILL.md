---
name: orchestrate
description: Route and coordinate bounded agent work with explicit ownership, cost, and verification.
---

# Orchestrate

Use for a task that benefits from coordination. Obtain mission, constraints,
authority, definition of done, and any adopted profile. Read the repository's
PLAYBOOK.md when available; this procedure also works as a standalone skill.

1. Separate coordination from execution. Keep small tasks with the lead. If
   delegation is permitted, define roles: planner decomposes; scout researches;
   worker implements; reviewer independently verifies; advisor recommends; lead
   integrates and owns acceptance.
2. Select the lowest verified capable tier, then concrete model and supported
   effort. Minimize expected cost per verified successful outcome, including latency,
   retries, and verification. Select provider, effort, permissions, and role explicitly.
   Without a verified roster, ask for a mapping or use the authorized lead.
3. For substantial Pi fan-outs, use `@parke.dev/pi-subagent` with `action: "plan"`
   where the installed version supports it. Inspect the resolved plan before
   launching; if unavailable, perform equivalent read-only checks without guessing
   dispatch syntax. Before Pi subagent dispatch, inspect the installed integration/version, actual
   agent definitions, resolved provider/model/effort, access, tools, isolation,
   concurrency, budgets, and fallback behavior. Confirm requested identities are
   available. Do not treat a package name or template as runtime proof.
4. For any harness, reject silent fallback or escalation. Honor operator overrides;
   explicit specialist requests fail closed. Never change credentials implicitly. A missing identity, unsupported effort,
   or changed billing route needs a visible diagnostic and an authorized choice.
5. Give each child a bounded objective, owned files or read-only scope, inputs,
   allowed actions, budget, stopping boundary, and evidence contract. Name agents
   according to the adopted profile. Bound parallelism to independent work and
   available capacity; isolate overlapping writes or serialize them.
6. Inspect results and integrate deliberately. Escalate uncertainty with evidence
   and a concrete proposed change. Stop at the agreed boundary. Distinguish a
   completed child task from completion of the overall objective.

Return decisions, actual identities used, validation, and unresolved work. Never
install integrations or widen merge/deployment authority merely to finish a task.

For adopted profiles, apply their concurrency and planner-effort defaults only
where supported. Without one, set an explicit bounded concurrency before launch.
For GitHub delivery or review, read the canonical PLAYBOOK.md section “GitHub
delivery and independent review.” If installed alone, obtain that public document
from the adopted playbook checkout or repository URL; do not invent its receipt.
This reference requires no Pi setup and grants no merge/deployment permission.
