# Rate Limiting

The built-in rate limiter slows a caller down before they crowd out everyone else.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Partitions

A limit per user, per API key, or per IP. Pick the identity you actually have.

## Algorithms

Fixed window, sliding window, token bucket, and concurrency.

## Rejection

A 429, a Retry-After header, and a body the client can read.

## Where it sits

A global limiter and an override on one endpoint.

## Authenticated callers

Limit the identity, not only the address, once a token is present.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Authorization](/csharp/aspnet-core/authorization/overview)

---

**Next:** [Pagination](/csharp/aspnet-core/web-apis/pagination)
