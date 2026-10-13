---
title: Reqnroll
order: 50
---

# Reqnroll

[Reqnroll](https://reqnroll.net) turns a Gherkin feature file into a test. On this site the test runner is TUnit, through the `Reqnroll.TUnit` package. Reqnroll supports TUnit 1.3.25 and later, on .NET 8 and later.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## In this section

- [Feature files](/csharp/testing/reqnroll/feature-files) - Gherkin: scenarios, outlines, tags, and backgrounds.
- [Step definitions](/csharp/testing/reqnroll/step-definitions) - Bindings from a step sentence to a method.
- [Hooks and context](/csharp/testing/reqnroll/hooks-and-context) - Setup, teardown, and injected state.
- [Living documentation](/csharp/testing/reqnroll/living-documentation) - The feature file as the spec that stays true.

## A feature

A `.feature` file a product owner can read. Given, When, Then.

## A binding

A C# method that runs one step.

## The package

`Reqnroll.TUnit` plus `TUnit`. Do not also add `Reqnroll.xUnit`.

## Parallelism

Scenarios run in parallel, because TUnit does. Opt out with `[assembly: TUnit.Core.NotInParallel]` or by excluding a feature.

## Test context

`TUnit.Core.TestContext` is available through Reqnroll context injection.

## .NET 10

The same `TestingPlatformDotnetTestSupport` property as any other TUnit project.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Feature files](/csharp/testing/reqnroll/feature-files)
- [Testing strategy](/sdlc/testing-strategy)
- [Requirements and stories](/sdlc/requirements-and-stories)

---

**Next:** [Feature Files](/csharp/testing/reqnroll/feature-files)
