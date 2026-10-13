---
title: Performance
order: 40
---

# Entity Framework Performance

Avoiding common performance pitfalls.

## N+1 Query Problem

<!-- TODO: What it is, how to detect, how to fix -->

## Tracking vs No-Tracking

<!-- TODO: AsNoTracking, when to use -->

## Compiled Queries

<!-- TODO: Pre-compiling frequent queries -->

## Batch Operations

<!-- TODO: Bulk insert/update/delete -->

## Connection Management

<!-- TODO: Connection pooling, async -->

## Profiling

<!-- TODO: Logging SQL, profiling tools -->

## Where the query actually runs

<!-- TODO: IQueryable vs IEnumerable boundary -->

## Existence checks and counting

<!-- TODO: Any translates to EXISTS, and counting pitfalls -->

## Projections versus loading entities

<!-- TODO: Select vs loading entities -->

## Bulk writes

<!-- TODO: ExecuteUpdate, ExecuteDelete, and AddRange batching -->

## Reading SQL logs

<!-- TODO: A review checklist for rows, query count, allocations, indexes, and the plan -->

## Practical Examples

- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - Performance in practice

---

**Continue to:** [ASP.NET Core](/csharp/aspnet-core/web-apis/overview)
