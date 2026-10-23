---
title: Overview
order: 1
---

# Chapter 6: API Development

Well-designed APIs are a pleasure to use. We'll build RESTful endpoints that are consistent, documented, and secure.

## What We'll Cover

- REST API design principles
- Controllers vs Minimal APIs
- Request validation
- Response formatting
- Error handling
- API versioning
- OpenAPI documentation (built-in generator, Scalar or Swagger UI)
- Rate limits per plan
- An MCP endpoint for tenants

## API Design Principles

<!-- TODO: Resource naming, HTTP methods, status codes -->

## Validation

<!-- TODO: FluentValidation, model validation -->

## Error Handling

<!-- TODO: Problem Details, global exception handling -->

## API Versioning

<!-- TODO: URL vs header versioning -->

## Documentation

<!-- TODO: Built-in OpenAPI document generation, with Scalar or Swagger UI -->

## Output caching

<!-- TODO: Output cache on read endpoints -->

## Keyset pagination

<!-- TODO: List endpoints use a keyset cursor -->

## Async request-reply

<!-- TODO: 202 Accepted and a status resource for work that outlives the request -->

## Idempotency keys

<!-- TODO: An Idempotency-Key header so a retried POST returns the first result -->

### Keys per tenant

- TODO: Store the key with the tenant. A unique index on tenant plus key keeps one tenant's retry from sharing another tenant's outcome.

## Rate limits per plan

- TODO: A free plan and a paid plan carry different limits. The partition includes the plan, along with the caller.
- TODO: Document the limit, the window, and what the client does with a 429.

## APIs called by agents

- TODO: Some commands are invoked by a model that picked a tool. Name the inputs, the errors, and whether a retry is safe.
- TODO: Require an idempotency key on those writes, and return the first result when the same key comes back.

### Scoping what an agent's key can touch

- TODO: The credential an agent uses can read the rows the task named and write to the store the task named. The rest of the API stays closed.
- TODO: The tenant and the date range are fixed on the task. A later turn cannot change them by asking.
- TODO: A call outside that scope fails in the API, including when the model requested it.

## An MCP endpoint for tenants

- TODO: A tenant-facing MCP endpoint is another API surface beside the HTTP API that agents call. It authenticates the caller and stays inside that tenant's data.
- TODO: Apply the same idempotency rule on its writes that the HTTP API uses.

### Hosted agent services as callers

- TODO: A tenant may connect a hosted agent service to this endpoint. That service is a caller, held to the same tenant boundary as a person using the API.
- TODO: Register the service you expect. A token from an unknown service is rejected.
- TODO: Host the endpoint so a remote service can call it, as in [Called by a hosted agent service](/csharp/mcp/hosting#called-by-a-hosted-agent-service).

## Outgoing webhooks for tenants

- TODO: A tenant registers a callback URL and a secret, and receives events for that tenant only.
- TODO: Sign the raw body with that subscriber's secret, and retry a delivery that failed until the attempt limit.
- TODO: Refuse a callback URL that resolves to a private or internal address before the request is sent.

## Related Topics

- See [ASP.NET Core: Web APIs](/csharp/aspnet-core/web-apis/overview)
- See [Rate limiting](/csharp/aspnet-core/web-apis/rate-limiting)
- See [MCP authentication](/csharp/mcp/authentication)
- See [APIs for agents](/csharp/aspnet-core/web-apis/apis-for-agents)
- See [Idempotent requests](/csharp/aspnet-core/web-apis/idempotent-requests)
- See [Webhooks](/csharp/aspnet-core/web-apis/webhooks)
- See [Caching](/csharp/aspnet-core/web-apis/caching)
- See [Caching fundamentals](/fundamentals/distributed-systems/caching)
- See [Pagination](/csharp/aspnet-core/web-apis/pagination)
- See [Polling, server-sent events, and async request-reply](/csharp/aspnet-core/web-apis/polling-sse-and-async-request-reply)

---

**Next:** [Chapter 7: Data Layer](/building-a-saas/07-data-layer/overview)
