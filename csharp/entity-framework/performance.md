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

### Counting round trips

- TODO: Each time the code walks an `IQueryable`, that walk is its own round trip. Walking the same query again pays again.
- TODO: Read the SQL log and count the trips before tuning the text of a single statement.

## Existence checks and counting

<!-- TODO: Any translates to EXISTS, and counting pitfalls -->

## Projections versus loading entities

<!-- TODO: Select vs loading entities -->

## Bulk writes

<!-- TODO: ExecuteUpdate, ExecuteDelete, and AddRange batching -->

## Reading SQL logs

<!-- TODO: A review checklist for rows, query count, allocations, indexes, and the plan -->

## Skewed tenant data

- TODO: A database where every tenant has a few rows hides the tenant that has millions.
- TODO: Seed one large tenant and assert the query shape, not only the small case.

## Large ID lists

- TODO: A filter over thousands of ids becomes one enormous `IN` list, or one query per id.
- TODO: Hand the ids to the database as a set it can join, in a single round trip.

## SaveChanges in a loop

- TODO: Saving on every iteration pays a transaction and a round trip per row.
- TODO: Stage the rows and save once, unless one row must commit before the next row starts.

## Streaming versus buffering

- TODO: Materialize a query once when later code needs the same rows. Walking it a second time sends it a second time.
- TODO: A streaming reader stays open until the loop finishes. Release it before an await that does other I/O, such as sending a notification.
- TODO: Buffer a small result you still need after the connection returns to the pool. Stream when holding every row would cost more than the extra round trips.

## Practical Examples

- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - Performance in practice
- See [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview) - Notification jobs
- See [Building a SaaS: Testing Strategy](/building-a-saas/10-testing-strategy/overview) - Test data for tenants of different sizes

---

**Continue to:** [ASP.NET Core](/csharp/aspnet-core/web-apis/overview)
