# Authentication

How an ASP.NET Core app establishes who the caller is. Pick the scheme on the choosing page before implementing any of the others.

## In this section

- [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme) - Cookies, JWT, OpenID Connect, and a backend-for-frontend. Key strength, a readable payload, and revocation decide which one fits.
- [ASP.NET Core Identity](/csharp/aspnet-core/authentication/identity) - Users, passwords, and the Identity store.
- [Cookie authentication](/csharp/aspnet-core/authentication/cookies) - The browser session for Blazor and server-rendered pages.
- [JWT bearer](/csharp/aspnet-core/authentication/jwt) - Tokens for services, MCP, and non-browser clients. Key strength, a readable payload, and revocation.
- [Refresh tokens](/csharp/aspnet-core/authentication/refresh-tokens) - Rotation and storage.
- [OpenID Connect](/csharp/aspnet-core/authentication/openid-connect) - An external identity provider.
- [Modern authentication](/csharp/aspnet-core/authentication/modern-auth) - Passkeys, device-bound sessions, and machine-to-machine calls.

## What changed in .NET 11

- TODO: Read the authentication and authorization notes for .NET 11 before copying a sample that was written for an older release.
- TODO: Name what a project on .NET 10 has to change when it moves: a renamed API, a new default, or a scheme registration that moved.
- TODO: The framework bump for this product is [Moving from 10 to 11](/building-a-saas/01-project-setup/overview#moving-from-10-to-11).

## Related

- [Authorization](/csharp/aspnet-core/authorization/overview)
- [Building a SaaS: Authentication](/building-a-saas/04-authentication/overview)

---

**Next:** [Choosing a Scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)
