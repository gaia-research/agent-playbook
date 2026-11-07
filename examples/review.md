# Example review brief

Input: PR <number-or-URL>, repository <owner/repo>, handoff <path>.
Mission: independently assess whether the pushed change meets its acceptance criteria.
Authority: read/fetch the PR and handoff; inspect source and run safe relevant
checks in an isolated checkout. Do not modify the PR, post comments, merge, or deploy.
Done: reviewed head SHA, evidence-backed findings, validation boundaries, and
approval/corrections recommendation. Use the review-pr skill.

A report that says “tests passed” is a claim. Reproduce relevant checks when
possible; otherwise label them as reported, and state what was independently
inspected. A changed remote head requires a new review or a scoped recommendation.
