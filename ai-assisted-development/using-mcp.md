# Using MCP

MCP lets an assistant call a tool on a server: read a ticket, query a database, or hit an API. Building the server is covered under C#.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Client and server

The assistant is the client. The tool you installed is the server.

## What a tool should do

One action, a clear description, and a result the model can quote.

## Permissions

A tool that can write or send is a different risk from a tool that can read.

## When to build one

A task you repeat, against a system that already has an API.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [MCP servers](/csharp/mcp/overview)
- [Terms](/ai-assisted-development/terms)

---

**Next:** [Risks and Limits](/ai-assisted-development/risks-and-limits)
