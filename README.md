# Agent Playbook

A small, memory-first, skills-second guide to directing AI work. Plain documents,
not an orchestration runtime. MIT licensed.

The portable policy is ready to read. [Marco's profile](profiles/marco/PROFILE.md)
records dated operator preferences and source-observed model candidates. Verify
local availability before dispatch; it does not provision providers or credentials.
See [the delivery handoff](HANDOFF.md) for evidence and limitations.

## Read conversationally

Start with [MEMORY.md](MEMORY.md), then [PLAYBOOK.md](PLAYBOOK.md). No installation
is needed. Suggested request:

> Read this Agent Playbook, load the relevant operating philosophy, and organize
> it into my memory. Ask before adopting a personal profile and confirm what your
> platform can actually persist.

Reading a repository does not itself save memory. Use the feature-branch URL
until a reviewed version is merged.

## Use in a coding harness

Choose either [orchestrate](skills/orchestrate/SKILL.md) or
[prompting](skills/prompting/SKILL.md). Handoff and independent review are
[playbook conventions](PLAYBOOK.md#github-delivery-and-independent-review), not
separate skills. Both skills work without Pi or any private infrastructure.

An agent should inspect the target harness version and supported skill format,
show the proposed files, destination, collisions, and any configuration changes,
then obtain explicit installation consent. Copy only selected skill directories
using that harness's documented discovery mechanism; preserve existing files and
verify discovery afterward. Do not install hooks, extensions, or dependencies as
a side effect. A manual conversation-context copy works without skill discovery.
Documented discovery locations and a consent-based installation recipe are in
[the harness notes](profiles/marco/harnesses.md).

## Personalize

Use [the profile template](profiles/template/PROFILE.md), or explicitly opt into
[Marco's profile](profiles/marco/PROFILE.md). Core skills must work with
either profile. The YAML files are playbook data, not native harness config.
See [harness boundaries](profiles/marco/harnesses.md) before adapting them.
The profile also records the conditional [Fable 5.2 preference and
provider-specific prompting guidance](profiles/marco/fable-5-2.md); it is not
a universal default or a proof of model availability.

Examples: [task](examples/task.md), [review](examples/review.md).
