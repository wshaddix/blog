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

## Key strength

- TODO: A bearer-token scheme depends on the key that signs the token. Pick a scheme whose key you can store outside the repo and rotate.
- TODO: A cookie session has a server-side key too. Give that key the same care.

## Readable payload

- TODO: Choose a cookie the browser will not show to script when the session contents have to stay on the server.
- TODO: Choose a JWT when the caller is a service that reads the claims. Those claims are visible to whoever holds the token.

## Immediate revocation

- TODO: Choose a server-side session when logout has to end access on the next request.
- TODO: Choose a short-lived JWT and a revocable refresh token when the caller cannot send a cookie.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Authentication concepts](/fundamentals/security/authentication-and-authorization)
- [Cookie authentication](/csharp/aspnet-core/authentication/cookies)
- [JWT](/csharp/aspnet-core/authentication/jwt)
- [Building a SaaS: Authentication](/building-a-saas/04-authentication/overview)

---

**Next:** [ASP.NET Core Identity](/csharp/aspnet-core/authentication/identity)
