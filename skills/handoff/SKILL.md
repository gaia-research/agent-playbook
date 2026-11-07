---
name: handoff
description: Deliver pushed implementation and committed evidence in a strict review receipt.
---

# Handoff

Use for authorized GitHub implementation delivery. Follow applicable project and
platform instructions; PLAYBOOK.md explains the repository's authority model.

1. Check scope and current branch. Review the diff for unintended or private data.
2. Run appropriate validation. Write a self-contained repository report covering
   implementation, validation commands/results, findings, and outstanding issues.
   Identify the implementation revision; avoid embedding a self-referential final
   commit SHA in the report. Never describe an unrun check as passing.
3. Commit implementation and report, push the feature branch, and create/update
   the PR when authorized. Verify remote HEAD and that the report exists at that
   revision. Do not merge or deploy without explicit authorization.
4. Report READY FOR REVIEW only when the authorized scope and delivery evidence
   are complete. Otherwise report BLOCKED and describe the blocker in the report.
   If there is no PR or pushed commit, use NONE with a short factual reason in
   the corresponding field; never substitute a local SHA for a pushed SHA.

Final response must contain exactly four lines:

```text
PR: <number and URL>
Commit: <pushed HEAD SHA>
Handoff: <repository-relative path>
Status: READY FOR REVIEW | BLOCKED
```
