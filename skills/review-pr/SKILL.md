---
name: review-pr
description: Independently verify a pushed PR and handoff without assuming merge authority.
---

# Review PR

Input: PR number or URL, repository identity if needed, and handoff path. Follow
applicable project/platform instructions and PLAYBOOK.md when available.

1. Resolve the PR's latest remote head and base. Fetch the handoff independently
   from that head; do not rely on a pasted report or an author's working tree.
2. Inspect the full diff and applicable repository instructions. Compare the
   mission and acceptance criteria against implementation and supporting evidence.
3. Run relevant checks when safe and available. Inspect test quality and coverage
   of changed behavior. Distinguish reproduced results, inspected evidence, author
   claims, and untested behavior. Review scripts before executing untrusted code.
4. Report actionable corrections with file/line evidence and impact, or recommend
   approval with scope and limitations. Report absent or stale handoff evidence
   explicitly. A green reported check is not verified correctness.
5. Recheck the remote head before concluding; if it changed, review the new diff
   or state that the recommendation applies only to the earlier SHA.

Return recommendation, reviewed SHA, findings, validation, and unresolved issues.
A recommendation is not permission to merge. Never merge without explicit
operator authorization; posting a review also requires authorized scope.
