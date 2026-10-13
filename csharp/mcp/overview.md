# MCP Servers

A Model Context Protocol server exposes tools, resources, and prompts to an AI client. In C# it is a hosted process, either on standard I/O or on HTTP.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## In this section

- [Tools, resources, and prompts](/csharp/mcp/tools-resources-and-prompts) - The three things a server exposes.
- [Hosting](/csharp/mcp/hosting) - stdio on the generic host, and HTTP on ASP.NET Core.
- [Authentication](/csharp/mcp/authentication) - Who may call a remote server.

## What the protocol is

A client, a server, and the messages between them.

## stdio and HTTP

A local process on stdin and stdout, or a remote server over HTTP.

## What you are building

A thin adapter over capabilities you already have, not a second business layer.

## The C# SDK

The official SDK, the host integration, and the attributes that describe a tool.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Tools, resources, and prompts](/csharp/mcp/tools-resources-and-prompts)
- [Using MCP from an assistant](/ai-assisted-development/using-mcp)

---

**Next:** [Tools, Resources, and Prompts](/csharp/mcp/tools-resources-and-prompts)
