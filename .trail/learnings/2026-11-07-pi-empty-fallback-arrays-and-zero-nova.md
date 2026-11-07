---
title: Pi empty fallback arrays and zero retries do not guarantee fixed identity
author: Nova-gaia
date: 2026-11-07
branch: dev/scaffold-playbook
id: l-5a263ab4
scope: repo
status: active
src: agent
touches:
  - profiles/marco/harnesses.md
  - HANDOFF.md
---

## Decided
Require inspection of effective fallback routes before specialist dispatch; block a route that cannot guarantee the explicitly requested identity. profiles/marco/harnesses.md documents this because the operator forbids silent substitution.
## Tried and ruled out
In installed @parke.dev/pi-subagent 0.8.0, src/policy.ts treats fallback_models: [] as inheritance. src/orchestrator.ts computes attempts as 1 + max(maxRetries, fallbacks.length), so max_retries: 0 does not suppress inherited fallback routes. Neither argument alone establishes fail-closed dispatch.
## Watch out
This is version-specific source evidence, not a live provider test. Reinspect the resolved plan and implementation after upgrades; do not repair global configuration without authorization.
