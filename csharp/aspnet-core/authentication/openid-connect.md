---
title: OpenID Connect
order: 140
---

# OpenID Connect

OpenID Connect is how WinUI, Uno, and a web app sign in with an external provider such as Microsoft Entra ID.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The code flow

The user signs in at the provider. The app receives a code.

## PKCE

A proof that the app that started the login is the app that finishes it.

## Tokens you get back

An id token, an access token, and often a refresh token.

## Redirect URIs

A URI per platform: a web origin, a Windows protocol, a mobile scheme.

## The API

The API trusts the provider's signing keys. It does not see the password.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Uno authentication](/csharp/uno/authentication)
- [WinUI authentication](/csharp/winui/authentication)

---

**Next:** [Modern Authentication](/csharp/aspnet-core/authentication/modern-auth)
