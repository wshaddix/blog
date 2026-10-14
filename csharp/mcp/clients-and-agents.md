---
title: MCP Clients and Agents
order: 50
---

# MCP Clients and Agents

An MCP client calls a server. An agent uses that client when a model asks for a tool.

## The MCP client

<!-- TODO: Open a session to a server and read its tools, resources, and prompts -->

### stdio and HTTP

<!-- TODO: A local process, or a remote server with the authentication that server requires -->

## IChatClient

<!-- TODO: Microsoft.Extensions.AI. The chat client is what the agent uses to talk to a model -->

## Tools the model can call

<!-- TODO: Expose the server's tools as functions on the chat client -->

## The tool loop

<!-- TODO: The model requests a call, the client runs it, and the result is sent back to the model -->

## A person in the loop

<!-- TODO: Confirm a tool that writes, pays, or sends before the client runs it -->

## More than one server

<!-- TODO: Several MCP servers on one agent, and tool names that stay unique -->

## Practical Examples

- See [Using MCP](/ai-assisted-development/using-mcp) - An assistant calling a server

## Related Topics

- See [MCP servers](/csharp/mcp/overview)
- See [Hosting an MCP server](/csharp/mcp/hosting)
- See [MCP authentication](/csharp/mcp/authentication)

---

**Next:** [Tools, Resources, and Prompts](/csharp/mcp/tools-resources-and-prompts)
