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

## In-process and distributed caches

An in-process cache stays on one server. A distributed cache is shared. See [HybridCache](/building-a-saas/07-data-layer/overview#hybridcache).

### Size limits

A cap on how much the in-process cache may hold.

### Mutable cached objects

A cached object that the caller can still change.

## HybridCache

### Local copies across servers

- TODO: Each server keeps an in-process copy in front of the shared cache.
- TODO: Removing or replacing the entry on one server leaves the other servers' copies in place until they expire.

### Empty results

A stored not-found is a cache entry. See [Not-found results](/building-a-saas/07-data-layer/overview#not-found-results).

### Setup with Redis as L2

### GetOrCreateAsync, tags, and stampede protection

### Invalidation strategies

## Measuring hit ratio

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Redis and caching](/databases/nosql/redis)
- [Caching](/fundamentals/distributed-systems/caching)

---

**Next:** [Web APIs](/csharp/aspnet-core/web-apis/overview)
