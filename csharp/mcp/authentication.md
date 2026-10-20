---
title: MCP Authentication
order: 10
---

# MCP Authentication

A local stdio server runs as the user. A remote HTTP server has to know who is calling.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Local servers

The process identity is the user's. Do not invent a second login.

## Remote servers

A bearer token or OAuth, and what the server checks on each call.

### Entra ID

- TODO: A remote MCP server can trust access tokens that Microsoft Entra ID issues for an API you register.
- TODO: The client asks for a token whose audience is that API. Accept the token when the audience matches this server.

### Token checks

- TODO: On each call, check the issuer, the audience, the lifetime, and the signature. Cache the signing keys, and refresh them when a signature fails.
- TODO: Map the token to the tenant the tool may read. Refuse the call when that mapping is missing.

## Authorization

A tool that reads one tenant's data has to enforce that boundary.

## Secrets

Tokens the server uses to call downstream APIs.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)
- [JWT](/csharp/aspnet-core/authentication/jwt)
- [Building a SaaS: API Development](/building-a-saas/06-api-development/overview)

---

**Next:** [MCP Servers](/csharp/mcp/overview)
