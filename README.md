# Agent Playbook

A small, memory-first, skills-second guide to directing AI work. Plain documents,
not an orchestration runtime. MIT licensed.

**Scaffold status:** the portable core is drafted from the supplied brief. Marco's
cloud conversation memory was unavailable. His model roster and historical
preferences are deliberately unresolved; this is not yet a plug-and-play profile.
See [the cloud-agent handoff](HANDOFF.md).

## Read conversationally

Start with [MEMORY.md](MEMORY.md), then [PLAYBOOK.md](PLAYBOOK.md). No installation
is needed. Suggested request:

> Read this Agent Playbook, load the relevant operating philosophy, and organize
> it into my memory. Ask before adopting a personal profile and confirm what your
> platform can actually persist.

Reading a repository does not itself save memory. Use the feature-branch URL
until a reviewed version is merged.

## Use in a coding harness

Choose individual skills: [orchestrate](skills/orchestrate/SKILL.md),
[prompting](skills/prompting/SKILL.md), [handoff](skills/handoff/SKILL.md), or
[review-pr](skills/review-pr/SKILL.md). Each has a standalone procedure; the
[playbook](PLAYBOOK.md) is the canonical authority reference.

An agent should inspect the target harness version and supported skill format,
show the proposed files, destination, collisions, and any configuration changes,
then obtain explicit installation consent. Copy only selected skill directories
using that harness's documented discovery mechanism; preserve existing files and
verify discovery afterward. Do not install hooks, extensions, or dependencies as
a side effect. A manual conversation-context copy works without skill discovery.
No installation commands are supplied as verified until the target is checked.

## Personalize

Use [the profile template](profiles/template/PROFILE.md), or explicitly opt into
[Marco's pending profile](profiles/marco/PROFILE.md). Core skills must work with
either profile. The YAML files are playbook data, not native harness config.
See [harness boundaries](profiles/marco/harnesses.md) before adapting them.

Examples: [task](examples/task.md), [review](examples/review.md).
