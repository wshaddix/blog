---
title: TUnit Project Setup
order: 100
---

# TUnit Project Setup

Tests on this site run on [TUnit](https://tunit.dev). A test project is an executable that discovers tests at compile time. It is not an xUnit, NUnit, or MSTest project.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Create the project

`dotnet new install TUnit.Templates`, then `dotnet new TUnit -n MyTests`. Run with `dotnet run --project MyTests`.

## The package

Reference the `TUnit` package. The project output type is `Exe`. Do not reference `Microsoft.NET.Test.Sdk`.

## Coverage

Use the coverage support that ships with TUnit. Do not add `coverlet`. It targets VSTest, and TUnit does not.

## Assertions

Assert with `await Assert.That(actual).IsEqualTo(expected)`. An assertion that is not awaited does not run, and the test can pass anyway.

## .NET 10

If `dotnet test` reports that VSTest is no longer supported, set `TestingPlatformDotnetTestSupport` to true in the project file.

## What a test looks like

A public class, a method marked `[Test]`, and no `[Fact]`, `[Theory]`, or `[TestMethod]`.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Unit testing](/csharp/testing/unit-testing)
- [Reqnroll](/csharp/testing/reqnroll/overview)

---

**Next:** [Unit Testing](/csharp/testing/unit-testing)
