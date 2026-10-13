# Redis and Caching

A cache and a short-lived store next to SQL Server. SQL remains the system of record.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## What to cache

Results that are read often, change rarely, and can be rebuilt.

## Keys and expiry

A key that includes the tenant, and a TTL so a stale value dies.

## Invalidation

Delete or replace the entry when the underlying row changes.

## What Redis is bad at

Queries, transactions across your domain, and data you cannot lose.

## From C#

A typed client, a timeout, and behavior when Redis is down.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [NoSQL overview](/databases/nosql/overview)
- [API caching](/csharp/aspnet-core/web-apis/caching)

---

**Next:** [NoSQL overview](/databases/nosql/overview)
