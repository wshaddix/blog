---
title: Data Protection
order: 10
---

# Data Protection

ASP.NET Core encrypts cookies and tokens with a key ring. More than one server means a shared ring.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## What it protects

Auth cookies, antiforgery tokens, and Identity tokens.

## A single server

Keys on disk, and what a redeploy does to them.

## More than one server

A shared location, or Key Vault, so every instance can decrypt.

## What a lost ring means

Every existing cookie becomes unreadable. Users sign in again.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Cookie authentication](/csharp/aspnet-core/authentication/cookies)

---

**Next:** [Secrets](/csharp/security/secrets)
