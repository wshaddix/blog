---
title: Tools
order: 80
---

# Tools

The categories of assistant you will meet. Product names change. The categories do not.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Chat

A conversation beside the editor. You paste context, or the tool attaches files you pick.

## Inline completion

A suggestion as you type. Fast, local to the cursor, and easy to accept without reading.

## IDE agent

An assistant inside the editor that can edit files and run commands in the workspace.

## CLI agent

The same kind of loop in a terminal, useful for a repo-wide change.

## Review bots

A pass over a pull request. A comment, not an approval.

## Running an agent without a chat

- TODO: A git hook or a pipeline job can start the agent with no one at the keyboard, and hand it the diff.
- TODO: Limit that run to a review comment on the change. Committing, merging, and widening the task stay with a person.

## Matching the model to the task

- TODO: A mechanical edit uses a smaller, faster model. Ordinary changes use the model the team picked for that work. A hard problem uses the stronger model.
- TODO: The strongest setting on every task is slow, and it tends to add structure the task did not ask for.
- TODO: Write the pairing down, so a new session does not start on the strongest setting.

## What to standardize

One primary agent for a team, a written instruction file, and a rule for secrets.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [Techniques](/ai-assisted-development/techniques)
- [CI/CD concepts](/devops/ci-cd/concepts)
- [Building a SaaS: Project Setup](/building-a-saas/01-project-setup/overview)

---

**Next:** [Techniques](/ai-assisted-development/techniques)
