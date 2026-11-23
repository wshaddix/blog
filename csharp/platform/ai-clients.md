---
title: AI Clients
order: 25
---

# AI Clients

Application code calls a model through one interface, then checks the answer the way it checks any other input.

## One seam

- TODO: Depend on `IChatClient`. The provider is a registration, not a type the feature names.
- TODO: Replacing the provider does not change the feature. See [Changing the model without changing the feature](/csharp/mcp/clients-and-agents#changing-the-model-without-changing-the-feature).

## Local and hosted

- TODO: Development points the client at a model on the developer machine. Production points the same client at a hosted endpoint.
- TODO: The address and the key come from configuration. The call site does not change between the two.

## Structured output

- TODO: Ask for a typed result, then validate that result the way a request body is validated.
- TODO: A payload that ignores the schema is a failed response, not a value to store.

## Rules the schema cannot say

- TODO: Check the business rules on the parsed value, such as totals that must add up and dates that must fall inside a range.
- TODO: A value that parses and still breaks a rule is rejected.

## When the check fails

- TODO: Retry or take a fallback when validation fails, and stop after a small number of attempts.
- TODO: Record the failure. Do not hand the unchecked text back to the caller.

## A prompt is a release

- TODO: Version the prompt with the build that sends it.
- TODO: Changing the prompt is a deploy. Run the checks in [Checking a model's answer](/building-a-saas/06-api-development/overview#checking-a-models-answer) before that build ships.

## Related Topics

- See [HTTP clients](/csharp/platform/http-clients)
- See [MCP clients and agents](/csharp/mcp/clients-and-agents)
- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview)

---

**Next:** [HTTP Clients](/csharp/platform/http-clients)
