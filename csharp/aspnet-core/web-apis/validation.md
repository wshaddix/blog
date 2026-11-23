---
title: Validation
order: 170
---

# Validation

Reject a request that cannot succeed before any state changes.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Data annotations

Attributes on the request type.

## FluentValidation

Rules that do not fit an attribute.

## Where the check runs

Automatic validation on minimal APIs and controllers.

## The error shape

A 400 whose body matches the Problem Details page.

## Localized messages

- TODO: The text comes from the attribute, from a resource key, or from the validator. The code that identifies the failure stays the same.
- TODO: Read the culture from the request and resolve the text for that culture.
- TODO: Assert one failure under two cultures: the same code, two different strings.
- TODO: How this API returns that pair is [A stable code and a localized message](/building-a-saas/06-api-development/overview#a-stable-code-and-a-localized-message).

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Attributes](/csharp/advanced-features/attributes)
- [Error handling](/csharp/aspnet-core/web-apis/error-handling)

---

**Next:** [Error Handling](/csharp/aspnet-core/web-apis/error-handling)
