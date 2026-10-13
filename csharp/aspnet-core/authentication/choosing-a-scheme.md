# Choosing a Scheme

The caller decides the scheme. A browser, a service, a Windows app, and a phone do not hold credentials the same way.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Browser apps

A cookie issued by the app. The browser stores it. Script does not read it.

## Services and MCP

A bearer JWT on each call.

## WinUI and Uno

Authorization code with PKCE against an identity provider. Tokens in secure storage.

## Backend for frontend

A browser that must call a JWT API talks to its own app, and the app holds the token.

## One API, several callers

The API validates a JWT. The web app can be a client of that API or the issuer of the cookie.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Authentication concepts](/fundamentals/security/authentication-and-authorization)
- [Cookie authentication](/csharp/aspnet-core/authentication/cookies)
- [JWT](/csharp/aspnet-core/authentication/jwt)

---

**Next:** [ASP.NET Core Identity](/csharp/aspnet-core/authentication/identity)
