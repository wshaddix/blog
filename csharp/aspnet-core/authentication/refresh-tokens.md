---
title: Refresh Tokens
order: 150
---

# Refresh Tokens

An access token is short-lived. A refresh token gets the next one without asking for the password again.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Why two tokens

A stolen access token dies quickly. A refresh token can be revoked.

## Rotation

Each refresh invalidates the previous token.

## Storage

A hash of the token on the server. Secure storage on a device. Never a log.

## Reuse detection

A rotated token that shows up again means the family is burned.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [JWT](/csharp/aspnet-core/authentication/jwt)
- [Client HTTP and auth](/csharp/clients/http-and-auth)

---

**Next:** [OpenID Connect](/csharp/aspnet-core/authentication/openid-connect)
