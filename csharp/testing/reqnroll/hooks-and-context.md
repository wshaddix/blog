---
title: Hooks and Context
order: 20
---

# Hooks and Context

Hooks set up a scenario. Context injection passes that setup into the steps.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Hooks

`[BeforeScenario]`, `[AfterScenario]`, and the feature and test-run equivalents.

## Context injection

A class Reqnroll constructs and passes to the bindings that ask for it.

## TUnit TestContext

Inject `TUnit.Core.TestContext` when a step needs the running test.

## Cleanup

An after-hook that runs when the scenario fails, not only when it passes.

## Scope

A hook that matches a tag, so a database scenario does not set up a database for every feature.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [TUnit project setup](/csharp/testing/project-setup)

---

**Next:** [Living Documentation](/csharp/testing/reqnroll/living-documentation)
