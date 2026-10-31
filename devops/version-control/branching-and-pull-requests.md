# Branching and Pull Requests

How a change moves from your machine onto `main`.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## A branch per change

Short-lived branches, and a name that says what the change is.

## Commits

Conventional commits, and a history someone can bisect.

## The pull request

Description, linked issue, and the checks that must pass.

### A description that points at the risk

A description can sort the diff by how much damage each part can do, so review time starts there.

- TODO: Ask the agent to group the change by risk, putting auth, data, and config ahead of renames and formatting.
- TODO: Compare that summary to the diff before treating it as the map of the change.
- TODO: Name the paths that still need a person, including when the summary calls them safe.
- TODO: Say what the summary is not evidence for, such as a claim that a sensitive file was untouched. See [A summary that ranks risk](/building-a-saas/01-project-setup/overview#a-summary-that-ranks-risk).

## Review and merge

Who approves, how conflicts are resolved, and when to squash.

## Rebase on shared branches

- TODO: Rebase a branch only while you are the only person using it.
- TODO: After someone else has pulled it, merge to take new commits from the base.
- TODO: A force-push after that rebase rewrites commits other people already have.

## What stays off the branch

Secrets, generated build output, and unrelated edits.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Git installation](/devops/version-control/git-installation)
- [Git recipes](/devops/version-control/git-recipes)
- [Conventional commits](/devops/version-control/conventional-commits)
- [Code review](/sdlc/code-review)
- [Building a SaaS: Project Setup](/building-a-saas/01-project-setup/overview)

---

**Next:** [Code Review](/sdlc/code-review)
