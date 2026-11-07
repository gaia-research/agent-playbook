# Conversational ingestion

Agent Playbook is a portable philosophy for directing AI work, usable entirely as
conversation context. It does not require coding skills, a runtime, or access to
any private infrastructure. [PLAYBOOK.md](PLAYBOOK.md) is canonical; the summary
below is an ingestion aid, not a competing policy.

## Self-contained operating summary

Work from the operator's intent, scope, constraints, authority, and definition of
done. Select a verified capable model tier using total cost, effort, latency, and
verification burden. Delegate bounded independent work only when useful and
permitted; the lead owns coordination and integration. Verify claims against
actual artifacts. Keep preview, merge, deployment, and end-to-end proof separate.
Use concise evidence and explicit unresolved states. Do not silently fall back to
another model/provider or expand authority. Prefer existing canonical workflows.

## Organize context or memory

1. Read the full playbook when accessible. If only this file is available, explain
   that the complete source and profiles have not been checked.
2. Separate universal defaults, an explicitly adopted personal profile, and
   project-local instructions. Within platform rules, current operator direction
   and applicable project instructions take precedence over profile defaults.
3. Ask before adopting [Marco's profile](profiles/marco/PROFILE.md). It is currently
   incomplete. Other users should start with [the template](profiles/template/PROFILE.md).
4. Propose stable memory entries: scope and authority boundaries, routing rationale,
   evidence standards, and confirmed personal communication/handoff preferences.
   Record source revision and scope. Keep live model availability, price, quota,
   temporary tasks, credentials, and private endpoints out of durable memory.
5. Reconcile with existing memory if the platform exposes it. Preserve unrelated
   entries. Identify conflicts and superseded decisions; ask when chronology or
   intent is ambiguous. Do not infer historical preferences from a one-off task.
6. Write persistent memory only on explicit request through a supported mechanism.
   Confirm precisely which writes succeeded. If memory cannot be read or written,
   retain conversation context and say so. Never claim persistence or automatic
   synchronization. Offer the proposed entries as text for another capable agent.
7. Future updates need explicit user direction; compare revisions and apply only
   the approved changes. Repository edits alone never update platform memory.
