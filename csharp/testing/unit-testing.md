---
title: Unit Testing
order: 90
---

# Unit Testing

A unit test checks one behavior of one type. Collaborators are replaced so the test does not touch a database, the network, or the clock. The runner is [TUnit](https://tunit.dev).

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Arrange, act, assert

Set up the object, call one method, and assert the outcome. A test that asserts several unrelated outcomes is two tests.

## What a test looks like

```csharp
public class PricingTests
{
    [Test]
    public async Task Applies_the_discount()
    {
        var pricing = new Pricing();

        var total = pricing.ApplyDiscount(100m, 0.10m);

        await Assert.That(total).IsEqualTo(90m);
    }
}
```

Assertions are asynchronous. An `Assert.That` that is not awaited does not run.

## Arguments

`[Arguments]` supplies another set of inputs to the same method. There is no `[Fact]` or `[Theory]`.

## Hooks

`[Before(Test)]` and `[After(Test)]` run around each test. Class, assembly, and session hooks exist for more expensive setup. Prefer a fresh object inside the test when setup is cheap.

## Names

The method name says the behavior: `Applies_the_discount`. The class name says the type under test.

## What stays out

A unit test does not open a connection or boot the web host. Those are the integration pages.

## Code example

The sample above is the shape. A longer sample will live in a companion `.cs` file next to this page.

## Related

- [TUnit project setup](/csharp/testing/project-setup)
- [Mocking](/csharp/testing/mocking)
- [Testing strategy](/sdlc/testing-strategy)

---

**Next:** [Mocking](/csharp/testing/mocking)
