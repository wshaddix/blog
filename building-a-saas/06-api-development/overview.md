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

## API Design Principles

## Validation

## Error Handling

## API Versioning

## Documentation

## Output caching

## Keyset pagination

## Async request-reply

## Idempotency keys

## APIs called by agents

- TODO: Some commands are invoked by a model that picked a tool. Name the inputs, the errors, and whether a retry is safe.
- TODO: Require an idempotency key on those writes, and return the first result when the same key comes back.

## Related Topics

- See [ASP.NET Core: Web APIs](/csharp/aspnet-core/web-apis/overview)
- See [APIs for agents](/csharp/aspnet-core/web-apis/apis-for-agents)
- See [Idempotent requests](/csharp/aspnet-core/web-apis/idempotent-requests)
- See [Caching](/csharp/aspnet-core/web-apis/caching)
- See [Pagination](/csharp/aspnet-core/web-apis/pagination)
- See [Polling, server-sent events, and async request-reply](/csharp/aspnet-core/web-apis/polling-sse-and-async-request-reply)

---

**Next:** [Chapter 7: Data Layer](/building-a-saas/07-data-layer/overview)
