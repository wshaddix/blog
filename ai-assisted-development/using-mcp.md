# Using MCP

MCP lets an assistant call a tool on a server: read a ticket, query a database, or hit an API. Building the server is covered under C#.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Client and server

The assistant is the client. The tool you installed is the server.

## What a tool should do

One action, a clear description, and a result the model can quote.

## Permissions

A tool that can write or send is a different risk from a tool that can read.

### Asking for more access mid-task

Begin with the smallest scope that can do the work, and widen it only when the task cannot continue.

- TODO: Start from that smallest scope, and add a permission only when the current one cannot finish the step.
- TODO: Describe how the server tells the client it needs a further permission.
- TODO: Say what the client should do when it can show that request, and what it should do when it cannot.
- TODO: Show the person the exact access being asked for, and write down every grant. See [Granting more scope later](/building-a-saas/06-api-development/overview#granting-more-scope-later).

## When to build one

A task you repeat, against a system that already has an API.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [MCP servers](/csharp/mcp/overview)
- [MCP clients and agents](/csharp/mcp/clients-and-agents)
- [Terms](/ai-assisted-development/terms)

---

**Next:** [Risks and Limits](/ai-assisted-development/risks-and-limits)
