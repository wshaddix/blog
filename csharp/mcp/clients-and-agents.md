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

### A local model in development

- TODO: In development the chat client calls a model running on the machine. In production the same client calls the hosted model.
- TODO: The endpoint and the credential come from configuration. The agent code does not branch on which environment it is in.
- TODO: Start that local model from the AppHost, as in [A local model as a dev resource](/building-a-saas/01-project-setup/overview#a-local-model-as-a-dev-resource).

### Typed results

- TODO: Ask the model for a value that matches a type or a schema, not an open-ended paragraph.
- TODO: Reject a payload that does not match, then retry or fail the turn on purpose.

## Tools the model can call

<!-- TODO: Expose the server's tools as functions on the chat client -->

## The tool loop

<!-- TODO: The model requests a call, the client runs it, and the result is sent back to the model -->

### Tracing the tool loop

- TODO: Start a span when the agent begins a turn, and add a child span for each tool call.
- TODO: Record the tool name, the duration, and whether the call succeeded. Leave argument values off the span when they hold tenant data.
- TODO: Keep the following model call on the same trace.

## A person in the loop

<!-- TODO: Confirm a tool that writes, pays, or sends before the client runs it -->

### Approval queue

- TODO: A draft that sends, pays, or writes waits until a person accepts it.
- TODO: The model does not perform the side effect. Accepting the draft does.

### Audit trail

- TODO: Store the draft, who decided, when, and the tool call that followed.
- TODO: Keep the record when the draft is rejected.

## A gate in front of every tool

The model may propose a tool call. The client decides whether that call is allowed.

### Data is not instructions

- TODO: A field on a row, a file, or a tool result is input. It does not add a rule for the run.
- TODO: Text that says to ignore the task, or to send the data somewhere else, stays data.
- TODO: Fix the limits when the run starts, such as the tenant and the date range, and keep those limits on a retry.

### Run state outside the model

- TODO: Store the run, its job id, and how far the work got, outside the model context, so a restart can resume from that record.
- TODO: After a call times out, read the recorded outcome before calling the tool again.
- TODO: Cap how long the run may last and how many times it may retry. A pending job is not done.

### Proof before done

- TODO: Done means the job succeeded and the expected output can be read. The model's last message is not that proof.
- TODO: Check the account, the dates, and the format before telling the caller the result is ready.
- TODO: Keep a check for the wrong account, for a restart in the middle, and for a job that succeeds without writing the output. Each check names the code that enforces it.

## More than one server

<!-- TODO: Several MCP servers on one agent, and tool names that stay unique -->

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
