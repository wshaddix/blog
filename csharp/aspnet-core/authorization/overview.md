# Authorization

Authorization runs after authentication. A valid token is not permission to do the thing.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Roles

A coarse group. Useful, and too coarse for most data.

## Claims

A fact about the caller that a policy can require.

## Policies

A named requirement, registered once, and applied to endpoints.

## Fallback policy

Authenticated by default. Anonymous is an explicit opt-out.

## Where to apply it

Endpoint metadata, controller attributes, and a check inside a handler when the rule needs the entity.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Authentication concepts](/fundamentals/security/authentication-and-authorization)
- [Permission-based authorization](/csharp/aspnet-core/authorization/permissions)
- [Resource-based authorization](/csharp/aspnet-core/authorization/resource-based)

---

**Next:** [Permission-Based Authorization](/csharp/aspnet-core/authorization/permissions)
