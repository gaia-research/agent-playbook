---
name: prompting
description: Write compact prompts with intent, constraints, authority, and observable completion criteria.
---

# Prompting

Use when writing or repairing an agent brief. Follow the repository's PLAYBOOK.md
when available and applicable platform/project instructions in all cases.

1. State the mission and why the result matters.
2. Supply authoritative inputs; label assumptions and untrusted reference content.
3. Define scope, constraints, permissions, and explicit stopping boundaries.
4. Define done using observable artifacts and appropriate validation.
5. For capable agents, specify outcomes and let them choose routine implementation
   details. For mechanical workers, specify exact transformations and checks.
6. Prefer an existing canonical skill/tool; avoid recreating its instructions.
7. Request concise output with useful evidence, revision identifiers, uncertainty,
   and outstanding issues. Remove procedural detail that does not reduce risk or
   resolve ambiguity. Do not hide necessary evidence to meet a brevity target.

Produce one usable brief. Do not execute its task unless execution was requested.
