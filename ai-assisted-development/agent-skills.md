---
title: Agent Skills
order: 55
---

# Agent Skills

A skill is a named procedure a tool can load. An instructions file is the set of rules that apply without being asked.

## Skill or instructions file

- TODO: Put a repeated procedure in a skill and invoke it by name.
- TODO: Leave a rule that applies to every task in the instructions file. See [Context and instructions](/ai-assisted-development/context-and-instructions).

## Where the files live

- TODO: Show the folder a skill occupies and which file the tool reads first.
- TODO: Keep one skill to one job, so loading it does not pull in the rest of the catalog.

## Staying aligned with the API

- TODO: When the API the skill calls changes, change the skill in the same edit.
- TODO: A skill that still describes the old route will be followed. Treat that as a broken instruction.

## Version and trust

- TODO: Version a skill with the package or the repository that ships it.
- TODO: Read a skill that arrived inside a package before enabling it. It runs with the permissions of the tool that loaded it.
- TODO: Where this product keeps those files is [Context and instructions](/building-a-saas/02-architecture-decisions/overview#context-and-instructions).

## Related Topics

- See [Context and instructions](/ai-assisted-development/context-and-instructions)
- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview)

---

**Next:** [Prompting](/ai-assisted-development/prompting)
