# Step Definitions

A step definition is a method whose attribute matches a sentence in the feature file.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Bindings

`[Binding]`, `[Given]`, `[When]`, and `[Then]`.

## Arguments

A word in the sentence that becomes a parameter, including a table.

## Sharing a phrase

One binding used by several features. A phrase that has drifted and should be one phrase.

## Async steps

A step that awaits I/O. Reqnroll generates async tests.

## Failures

An assertion with `Assert.That`, so the failure reads like any other TUnit failure.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Unit testing](/csharp/testing/unit-testing)

---

**Next:** [Hooks and Context](/csharp/testing/reqnroll/hooks-and-context)
