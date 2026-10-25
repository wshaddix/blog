# Indexes and Query Plans

Why a query is fast or slow, and how an index changes the plan.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## What an index is

A structure the engine uses to find rows without reading the whole table.

## Clustered and nonclustered

How SQL Server stores the table, and what a secondary index costs on write.

## Reading a plan

Seeks, scans, lookups, and the estimate versus the actual row count.

## Indexes that match the query

The columns you filter, join, and sort on.

### Equality columns then the sort

Put equality columns first and the sort column after them; an index that leads with an unrelated column still shows a sort operator, and the extra index costs writes and storage.

## When not to add one

Write cost, unused indexes, and a query that needs a rewrite instead.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [SQL Server](/databases/relational/sql-server/overview)
- [Entity Framework performance](/csharp/entity-framework/performance)

---

**Next:** [Transactions and Isolation](/databases/relational/transactions-and-isolation)
