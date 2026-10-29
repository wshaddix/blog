# MCP Clients and Agents

An MCP client calls a server. An agent uses that client when a model asks for a tool.

## The MCP client

### stdio and HTTP

## IChatClient

### A local model in development

- TODO: In development the chat client calls a model running on the machine. In production the same client calls the hosted model.
- TODO: The endpoint and the credential come from configuration. The agent code does not branch on which environment it is in.
- TODO: Start that local model from the AppHost, as in [A local model as a dev resource](/building-a-saas/01-project-setup/overview#a-local-model-as-a-dev-resource).

### Typed results

- TODO: Ask the model for a value that matches a type or a schema, not an open-ended paragraph.
- TODO: Reject a payload that does not match, then retry or fail the turn on purpose.

### Changing the model without changing the feature

- TODO: Keep the model behind `IChatClient` and configuration, keep tools, rules, and review screens independent of the provider, and run the same evals against the replacement before switching.

### Reusing answers to similar questions

- TODO: Reuse an earlier model answer for a similar question. See [Reusing model answers](/building-a-saas/07-data-layer/overview#reusing-model-answers).

### The smallest model that passes

- TODO: Write the evals first. A model passes when it meets that set.
- TODO: Start with a small model and step up to a larger one only when the evals fail.
- TODO: Compare the cost and the latency of one call, along with the quality.
- TODO: Run that comparison again when the model or the prompt changes. See [Trying smaller models](/building-a-saas/10-testing-strategy/overview#trying-smaller-models).

## Tools the model can call

### Return a reference, not the bytes

- TODO: A tool that returns a whole row places every column in the model context, whether the question needed that column or not.
- TODO: Images and other binaries spend the context window and the token budget on content the model does not read as text.
- TODO: Return an identifier and a little metadata, and offer a second tool that fetches the content when the turn needs it.
- TODO: If an image does have to come back, shrink it to a thumbnail first.
- TODO: Log how large each tool result is. See [Files an agent reads](/building-a-saas/07-data-layer/overview#files-an-agent-reads).

## The tool loop

### Tracing the tool loop

- TODO: Start a span when the agent begins a turn, and add a child span for each tool call.
- TODO: Record the tool name, the duration, and whether the call succeeded. Leave argument values off the span when they hold tenant data.
- TODO: Keep the following model call on the same trace.

### A cap on round trips

- TODO: Each round trip is another model call, so it costs latency and tokens.
- TODO: The default cap is 40, including the first call. It is high so a task that needs several tool calls can finish.
- TODO: Set the number from a successful run of the real flow, a little above how many calls that run made.
- TODO: On the last allowed round trip the tools are left off the request, and the caller gets that final answer instead of another tool request.
- TODO: Log when a turn reaches the cap. Hitting it is a sign the prompt or the tools are confusing the model.
- TODO: Count those calls on the request. See [Model calls per request](/building-a-saas/12-monitoring-operations/overview#model-calls-per-request).

## A person in the loop

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
