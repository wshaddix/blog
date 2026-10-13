---
title: JWT Bearer
order: 160
---

# JWT Bearer

A JSON Web Token is a signed set of claims. The API checks the signature, the issuer, the audience, and the expiry.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Claims

Subject, name, roles, and a tenant id.

## Signing

A key, an algorithm, and who holds the private material.

## Validation

Issuer, audience, lifetime, and clock skew.

## Where a browser must not put it

Local storage is readable by script. See choosing a scheme.

## Passing the token

An Authorization header. Nothing else.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Refresh tokens](/csharp/aspnet-core/authentication/refresh-tokens)
- [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)

---

**Next:** [Refresh Tokens](/csharp/aspnet-core/authentication/refresh-tokens)
