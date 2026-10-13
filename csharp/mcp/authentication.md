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

## Authorization

A tool that reads one tenant's data has to enforce that boundary.

## Secrets

Tokens the server uses to call downstream APIs.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)
- [JWT](/csharp/aspnet-core/authentication/jwt)

---

**Next:** [MCP Servers](/csharp/mcp/overview)
