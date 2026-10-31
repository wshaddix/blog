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

### Why not GraphQL

This API is a set of resource endpoints. A query the client shapes is a later decision.

- TODO: The screens we ship are covered by those endpoints. A second contract would have to be versioned and authorized on its own.
- TODO: Nested fields would need batched lookups and a cost limit before they were safe to expose. See [GraphQL](/csharp/aspnet-core/web-apis/graphql).

### One set of JSON options

Every endpoint should serialize with the same JSON options.

- TODO: Set naming, nulls, and converters once, and keep a second code path from building its own copy.
- TODO: Measure before replacing the serializer the framework already uses. See [Configuring options once](/csharp/aspnet-core/web-apis/json-serialization#configuring-options-once).

## Validation

<!-- TODO: FluentValidation, model validation -->

## Error Handling

<!-- TODO: Problem Details, global exception handling -->

## Request timeouts

- TODO: Bound how long one request may run, and pass that limit into the work. See [Request timeouts](/csharp/advanced-features/cancellation#request-timeouts).

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

## Conditional updates

- TODO: Two admins of one tenant open the same settings page. The second save must not erase the first.
- TODO: The settings endpoint returns an ETag and requires `If-Match` on save. A stale save gets 412, and the page reloads the current values. See [Conditional requests](/csharp/aspnet-core/web-apis/conditional-requests).

## Idempotency keys

<!-- TODO: An Idempotency-Key header so a retried POST returns the first result -->

### Keys per tenant

- TODO: Store the key with the tenant. A unique index on tenant plus key keeps one tenant's retry from sharing another tenant's outcome.

## Bulk imports

- TODO: A tenant uploads thousands of records in one request. Stream the items and save them in batches instead of binding one array. See [Large request bodies](/csharp/aspnet-core/web-apis/routing-and-binding#large-request-bodies).
- TODO: The size limit can follow the tenant's plan.

## Rate limits per plan

- TODO: A free plan and a paid plan carry different limits. The partition includes the plan, along with the caller.
- TODO: Document the limit, the window, and what the client does with a 429.

### Counters shared across instances

- TODO: Every instance reads and updates the same counters for a plan. See [More than one instance](/csharp/aspnet-core/web-apis/rate-limiting#more-than-one-instance).

## APIs called by agents

- TODO: Some commands are invoked by a model that picked a tool. Name the inputs, the errors, and whether a retry is safe.
- TODO: Require an idempotency key on those writes, and return the first result when the same key comes back.

### Scoping what an agent's key can touch

- TODO: The credential an agent uses can read the rows the task named and write to the store the task named. The rest of the API stays closed.
- TODO: The tenant and the date range are fixed on the task. A later turn cannot change them by asking.
- TODO: A call outside that scope fails in the API, including when the model requested it.

### Granting more scope later

The key starts narrow. A later step can ask for a further permission when the first grant is not enough.

- TODO: Keep the first grant to the task as it was written. Ask for more only when that scope cannot do the next step.
- TODO: The person sees the extra scope before it is added, and the grant is recorded. See [Asking for more access mid-task](/ai-assisted-development/using-mcp#asking-for-more-access-mid-task).

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
- See [Cancellation](/csharp/advanced-features/cancellation)
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
