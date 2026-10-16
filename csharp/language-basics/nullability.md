# Nullability

Nullable reference types make a missing value visible at compile time.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Reference types and null

What `null` means, and the bugs it used to hide.

## Annotations

`string` and `string?`. The compiler warnings that follow.

## The null-forgiving operator

When `!` is a promise, and when it hides a bug.

## Patterns

`is null`, `??`, and `?.`.

### Empty collections

- TODO: Return an empty array or list when the result is "no items."
- TODO: Keep null for a value that was never supplied. Callers should not treat "nothing matched" as a missing value.

## Project setting

`<Nullable>enable</Nullable>` and why new projects turn it on.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Types and Variables](/csharp/language-basics/types)

---

**Next:** [Exceptions](/csharp/language-basics/exceptions)
