---
title: One Repo or Many
order: 11
---

# One Repo or Many

One repository or a repository per service is a choice about how code is shared.

## Sharing code

Repository layout decides which code can change together. How each service is deployed is a separate choice.

- TODO: Write the repository decision as a code-sharing decision.
- TODO: Record deployment on its own, including a service that runs in its own process while its code stays in this repository.

## A contract change in one pull request

One repository lets the contract, the producer, and the consumers move together.

- TODO: Land the contract change, the producer, and every consumer in one pull request.
- TODO: Run the cross-service integration tests on a developer machine against that same change.

## The cost of staying together

A single repository stays workable when the build, the reviewers, and the checkout stay bounded.

- TODO: Configure CI so a change builds and tests only the projects it touches.
- TODO: Give each folder code owners so review still has a named owner.
- TODO: Watch clone size and build time, and treat growth there as the cost of one repository.

## A pipeline and a version per service

Services that share a repository can still ship on their own.

- TODO: Give each service its own pipeline.
- TODO: Version each service separately, so one service can release without releasing the others.

## Code outside the workspace

An agent edits the files the workspace contains. A contract that is not there is invented.

- TODO: Keep the contracts an agent must change inside the workspace.
- TODO: Treat a missing contract as a guess, and say so in review. See [Code the agent can't see](/ai-assisted-development/context-and-instructions#code-the-agent-cant-see).

## Signals to split

Split the repository when the people, the releases, or the access rules have already split.

- TODO: Split when separate teams own the services.
- TODO: Split when the services release on different cadences.
- TODO: Split when an access boundary means some people must not see the other code.
- TODO: After a module leaves the process, the repository question for this product is [Staying in one repo after a module leaves](/building-a-saas/02-architecture-decisions/overview#staying-in-one-repo-after-a-module-leaves).

## Related Topics

- See [Branching and pull requests](/devops/version-control/branching-and-pull-requests)
- See [Context and instructions](/ai-assisted-development/context-and-instructions)
- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview)

---

**Next:** [CI/CD Concepts](/devops/ci-cd/concepts)
