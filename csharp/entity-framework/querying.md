# Querying with Entity Framework

Using LINQ to query databases.

## Basic Queries

## Loading Related Data

## Full outer joins

- TODO: A full outer join keeps the rows that match and the rows that have no partner on the other side.
- TODO: Use it for a reconciliation that has to show what exists only on the left and what exists only on the right.
- TODO: Assert the SQL text, not only the materialized rows, so a later EF version cannot change the shape unnoticed.
- TODO: Where this product needs that report is [Several collections on one parent](/building-a-saas/07-data-layer/overview#several-collections-on-one-parent).

## Projections

## Filtering and Sorting

## Pagination

### Offset versus keyset

### Composite index design

### Opaque cursor encoding

### API response shape

## Raw SQL

## Practical Examples

- See [C#: LINQ](/csharp/advanced-features/linq) - LINQ fundamentals

---

**Next:** [Migrations](/csharp/entity-framework/migrations)
