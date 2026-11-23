---
title: Error Handling
order: 160
---

# Error Handling

One error shape for the whole API, so every client parses failures the same way.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Problem Details

RFC 9457, `type`, `title`, `status`, and `detail`.

## Known failures

A domain error mapped to a status code.

- TODO: Represent the failures the domain has already named as a union, and map each case to a status code.
- TODO: A failure the union does not contain is an unknown failure, handled in the next section.
- TODO: The domain side of that union is [Result-style errors](/building-a-saas/03-domain-modeling/overview#result-style-errors) and [Unions on hot paths](/csharp/advanced-features/modern-csharp#unions-on-hot-paths).

## Unknown failures

A global handler, a log, and a body that does not leak internals.

## Validation errors

Field errors inside the same document.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Exceptions](/csharp/language-basics/exceptions)

---

**Next:** [OpenAPI](/csharp/aspnet-core/web-apis/openapi)
