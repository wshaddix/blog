---
title: Code Review
order: 50
---

# Code Review

How a change gets read before it merges.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## What a review is for

Correctness, design, and operability. Style that a formatter already enforces.

## The pull request

A description, the test that covers the change, and a size someone can read.

## Reading a diff

Start at the test, then the public API, then the implementation.

## Generated code

AI-written changes get the same review as any other change.

## Feedback

A comment that names the problem and the outcome you want.

## Changes that need a second reviewer

- TODO: Judge the risk by the area the change touches, not by the size of the diff.
- TODO: Authorization, billing, migrations, and secrets get a second reviewer.
- TODO: Route those paths with a code-owners file so the request reaches the right person.
- TODO: Let an agent flag a diff that touches one of those areas.
- TODO: Keep the list of areas short so a second review stays rare. See [Reviewing authorization changes](/building-a-saas/04-authentication/overview#reviewing-authorization-changes).

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Branching and pull requests](/devops/version-control/branching-and-pull-requests)
- [AI-assisted verification](/ai-assisted-development/verification)

---

**Next:** [Architecture](/sdlc/architecture)
