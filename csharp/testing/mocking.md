---
title: Mocking
order: 80
---

# Mocking

A mock stands in for a collaborator so the test can decide what that collaborator returns and can check that it was called. This site uses [TUnit.Mocks](https://tunit.dev/docs/writing-tests/mocking).

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The package

`TUnit.Mocks`. It generates the mock at compile time, so it works with trimming and Native AOT. It requires C# 14 (`LangVersion` of `14` or `preview`).

`TUnit.Mocks.Http` and `TUnit.Mocks.Logging` cover `HttpClient` and `ILogger`.

## What a mock looks like

```csharp
public class GreeterTests
{
    [Test]
    public async Task Greet_Returns_Configured_Value()
    {
        var mock = IGreeter.Mock();
        mock.Greet(Any()).Returns("Hello!");

        IGreeter greeter = mock;
        var result = greeter.Greet("Alice");

        await Assert.That(result).IsEqualTo("Hello!");
        mock.Greet("Alice").WasCalled(Times.Once);
    }
}
```

The mock is the interface. There is no `.Object` you have to remember, though `.Object` exists.

## Loose and strict

Loose is the default: an unconfigured call returns a default. Strict throws. Set strict on one mock, or as the default in a `[Before(HookType.TestDiscovery)]` hook.

## What to mock

Interfaces at the edge of the type under test: a clock, a mailer, an HTTP API.

## What not to mock

The type under test, a value object, or a `DbContext` when the test claims to prove a query. Query tests use a real database provider. See [Testing Entity Framework](/csharp/entity-framework/testing).

## Code example

The sample above is the shape. A longer sample will live in a companion `.cs` file next to this page.

## Related

- [Unit testing](/csharp/testing/unit-testing)
- [TUnit project setup](/csharp/testing/project-setup)

---

**Next:** [Time-Dependent Code](/csharp/testing/time-dependent-code)
