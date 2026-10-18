---
title: Caching
order: 80
---

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

<!-- TODO: Fix the query first. See [Entity Framework performance](/csharp/entity-framework/performance). -->

## Cache options

<!-- TODO: In-process, distributed, hybrid, output, and response: scope, consistency, and cost -->

## HybridCache

<!-- TODO: One API over a local cache and a distributed cache -->

### Local copies across servers

- TODO: Each server keeps an in-process copy in front of the shared cache.
- TODO: Removing or replacing the entry on one server leaves the other servers' copies in place until they expire.

### Setup with Redis as L2

<!-- TODO -->

### GetOrCreateAsync, tags, and stampede protection

<!-- TODO -->

### Invalidation strategies

<!-- TODO: Tag on write, TTL, versioned keys -->

## Measuring hit ratio

<!-- TODO: Hit ratio, latency, and memory -->

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Redis and caching](/databases/nosql/redis)
- [Caching](/fundamentals/distributed-systems/caching)

---

**Next:** [Web APIs](/csharp/aspnet-core/web-apis/overview)
