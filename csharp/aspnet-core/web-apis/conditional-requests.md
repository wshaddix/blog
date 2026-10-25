# Conditional Requests

Two clients edit the same resource. The second save should fail instead of erasing the first.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The version a client saw

- TODO: Return an `ETag` header on a GET. Derive it from the row's concurrency token, not from a hash of the whole body.
- TODO: The client keeps that value and sends it back when it saves.

## If-Match on a write

- TODO: A PUT, PATCH, or DELETE carries `If-Match` with the ETag the client last read.
- TODO: Compare it with the stored version inside the same save, so the check and the write cannot drift apart. See [Optimistic concurrency](/csharp/entity-framework/concurrency#optimistic-concurrency).

## Status codes

- TODO: A stale `If-Match` gets 412 Precondition Failed. The client reloads and decides what to keep.
- TODO: A write that arrives without `If-Match` on a resource that requires it gets 428 Precondition Required.
- TODO: Send the error as Problem Details, like every other failure. See [Error handling](/csharp/aspnet-core/web-apis/error-handling).

## If-None-Match on a read

- TODO: The same ETag lets a GET answer 304 Not Modified. That saves bandwidth. It does not protect a write.

## Practical Examples

- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview#conditional-updates) - Two admins editing one tenant's settings

## Related Topics

- See [Concurrency](/csharp/entity-framework/concurrency)
- See [Idempotent requests](/csharp/aspnet-core/web-apis/idempotent-requests)
- See [HTTP and the Web](/fundamentals/networking/http#caching-headers)

---

**Next:** [Minimal APIs and Controllers](/csharp/aspnet-core/web-apis/minimal-apis-and-controllers)
