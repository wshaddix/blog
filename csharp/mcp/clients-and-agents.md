# MCP Clients and Agents

An MCP client calls a server. An agent uses that client when a model asks for a tool.

## The MCP client

### stdio and HTTP

## IChatClient

### Typed results

- TODO: Ask the model for a value that matches a type or a schema, not an open-ended paragraph.
- TODO: Reject a payload that does not match, then retry or fail the turn on purpose.

## Tools the model can call

## The tool loop

### Tracing the tool loop

- TODO: Start a span when the agent begins a turn, and add a child span for each tool call.
- TODO: Record the tool name, the duration, and whether the call succeeded. Leave argument values off the span when they hold tenant data.
- TODO: Keep the following model call on the same trace.

## A person in the loop

### Approval queue

- TODO: A draft that sends, pays, or writes waits until a person accepts it.
- TODO: The model does not perform the side effect. Accepting the draft does.

### Audit trail

- TODO: Store the draft, who decided, when, and the tool call that followed.
- TODO: Keep the record when the draft is rejected.

## More than one server

## Practical Examples

- See [Using MCP](/ai-assisted-development/using-mcp) - An assistant calling a server
- See [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview) - Work that waits for a person

## Related Topics

- See [MCP servers](/csharp/mcp/overview)
- See [Hosting an MCP server](/csharp/mcp/hosting)
- See [MCP authentication](/csharp/mcp/authentication)
- See [Observability](/csharp/aspnet-core/observability/overview)

---

**Next:** [Tools, Resources, and Prompts](/csharp/mcp/tools-resources-and-prompts)
