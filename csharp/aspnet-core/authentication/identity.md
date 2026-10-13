---
title: ASP.NET Core Identity
order: 180
---

# ASP.NET Core Identity

Identity stores users, passwords, and roles. It is the user database, not the wire protocol.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The user type

A custom user class and the fields you add.

## Registration and password storage

Hashing, and the rules for a password.

## Email confirmation and reset

Tokens that expire, and the mail that carries them.

## Sign-in manager

How a password check becomes a principal.

## Where JWT fits

Identity checks the password. A separate issuer mints the token.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Building a SaaS: Authentication](/building-a-saas/04-authentication/overview)

---

**Next:** [Cookie Authentication](/csharp/aspnet-core/authentication/cookies)
