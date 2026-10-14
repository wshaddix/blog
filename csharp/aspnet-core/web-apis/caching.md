# Caching

Cache a response when the bytes do not depend on a side effect.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Output cache

Store the rendered response on the server.

## Response caching

Headers that tell a client or a proxy to store the response.

## What varies

A cache key that includes the user or the tenant when the body does.

## Invalidation

A write that makes a cached read wrong.

## Before you cache

## Cache options

## HybridCache

### Setup with Redis as L2

### GetOrCreateAsync, tags, and stampede protection

### Invalidation strategies

## Measuring hit ratio

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Redis and caching](/databases/nosql/redis)

---

**Next:** [Web APIs](/csharp/aspnet-core/web-apis/overview)
