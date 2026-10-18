# Caching

A cache keeps a copy so you can skip the slower read, and then you have to live with that copy being old.

## Eviction

- TODO: The cache has a limit. When it is full, an entry already stored has to leave before a new one fits.
- TODO: Name the rule that chooses the victim, and what the caller does on the miss that follows.

## Hit rate and eviction rate

- TODO: A hit is a read answered from the copy. An eviction is an entry dropped before the next read wanted it.
- TODO: Count both. A cache can answer most reads and still be throwing entries away as fast as it stores them.

## Misses under load

- TODO: Every miss falls through to the origin. A cold or flushed cache turns a spike of traffic into a spike of origin reads.
- TODO: Share one origin read across callers waiting on the same key, and cap how hard a cold cache may hit the origin.

## Warm-up

- TODO: A process start or a flush begins empty, so the first wave of traffic is all misses.
- TODO: Load the keys you already know you need, and decide which keys are too many to warm.

## Granularity

- TODO: An entry can be one field, one row, or a whole response. A larger entry is fewer keys and a costlier refresh.
- TODO: Cache the smallest piece that still saves the work. A coarse entry is stale as soon as any part of it changes.

## Practical Examples

- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview) - Output caching
- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - HybridCache
- See [Building a SaaS: Monitoring and Operations](/building-a-saas/12-monitoring-operations/overview) - Cache health

## Related Topics

- See [Consistency](/fundamentals/distributed-systems/consistency)
- See [Caching in ASP.NET Core](/csharp/aspnet-core/web-apis/caching)
- See [Redis](/databases/nosql/redis)

---

**Next:** [Failure and Degradation](/fundamentals/distributed-systems/failure-and-degradation)
