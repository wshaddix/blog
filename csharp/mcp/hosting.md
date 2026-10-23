---
title: Hosting an MCP Server
order: 20
---

# Hosting an MCP Server

The same server can run as a local stdio process or as an HTTP endpoint.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## stdio

A generic host whose transport is stdin and stdout. Logging stays off stdout.

## HTTP

ASP.NET Core hosting for a remote client.

## Registration

How tools in an assembly are discovered and added to the server.

## Lifetime

Startup, shutdown, and a server that outlives one request.

## Testing

A TUnit test that boots the server and calls a tool.

## Called by a hosted agent service

- TODO: A hosted agent service is a remote client of the HTTP server. It is not a stdio process this host starts.
- TODO: Accept a token from a service this server has registered. Reject a caller it does not know.
- TODO: That service can run only the tools this server published, and each argument still has to pass the server's own checks.
- TODO: When the product is multi-tenant, bind the caller to one tenant. See [Hosted agent services as callers](/building-a-saas/06-api-development/overview#hosted-agent-services-as-callers).

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Generic host](/csharp/platform/generic-host)
- [TUnit project setup](/csharp/testing/project-setup)
- [Building a SaaS: API Development](/building-a-saas/06-api-development/overview) - A tenant MCP endpoint called by a hosted agent service

---

**Next:** [MCP Authentication](/csharp/mcp/authentication)
