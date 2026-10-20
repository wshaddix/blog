# Rate Limiting

The built-in rate limiter slows a caller down before they crowd out everyone else.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Partitions

A limit per user, per API key, or per IP. Pick the identity you actually have.

## Algorithms

Fixed window, sliding window, token bucket, and concurrency.

### Fixed window

- TODO: Count calls inside a window that opens on a clock boundary, such as the start of a minute.
- TODO: The counter returns to zero when the window ends, so traffic at the end of one window and the start of the next is counted apart.

### Sliding window

- TODO: Combine the current window with the unused portion of the previous window, weighted by how far the current window has moved.
- TODO: A burst that crosses the boundary still counts against the limit.

### Token bucket

- TODO: The bucket holds tokens and refills at a steady rate. A call spends a token.
- TODO: The bucket size is the burst you allow. The refill rate is the sustained rate.

### Concurrency

- TODO: Count calls in flight. A slot frees when the call finishes, independent of the clock.
- TODO: Use it when the scarce resource is work happening at once, such as one expensive endpoint.

## Choosing per endpoint

- TODO: Keep a global limit for the process, and give an expensive or sensitive endpoint its own policy.
- TODO: Name the partition that endpoint uses: user, API key, address, or plan. An anonymous route can partition only on what the request already carries.

## Queueing

- TODO: Queue a call that arrives over the limit until a slot frees, up to a maximum number of waiting calls and a maximum wait.
- TODO: Past that cap, reject the call with 429 and a Retry-After value the client can honor.

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
- [Building a SaaS: API Development](/building-a-saas/06-api-development/overview)

---

**Next:** [Pagination](/csharp/aspnet-core/web-apis/pagination)
