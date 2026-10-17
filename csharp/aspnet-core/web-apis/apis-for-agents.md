---
title: APIs for Agents
order: 215
---

# APIs for Agents

An HTTP API whose caller is a model choosing a tool.

## A contract a tool can call

- TODO: Name each operation, its inputs, and its errors so they can become a tool definition.
- TODO: Keep one way to do a thing. Two routes for the same write give the model two guesses.

## Errors the caller can act on

- TODO: Return a stable error code and a short reason.
- TODO: Say whether the call is safe to retry.

## Auth for a non-human caller

- TODO: The agent presents a credential the API can revoke.
- TODO: Scope that credential to the tenant and to the operations that agent may run.

## Idempotent writes

- TODO: Expect the model to send a write twice. Require an idempotency key on commands.
- TODO: Return the stored result when the same key arrives again.

## Practical Examples

- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview) - Commands an agent may retry

## Related Topics

- See [Idempotent requests](/csharp/aspnet-core/web-apis/idempotent-requests)
- See [MCP clients and agents](/csharp/mcp/clients-and-agents)
- See [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)

---

**Next:** [Idempotent Requests](/csharp/aspnet-core/web-apis/idempotent-requests)
