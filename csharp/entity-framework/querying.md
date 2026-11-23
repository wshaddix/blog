---
title: Querying
order: 80
---

# Querying with Entity Framework

Using LINQ to query databases.

## Basic Queries

<!-- TODO: Find, Where, Single, First -->

## Loading Related Data

<!-- TODO: Eager loading (Include), explicit loading, lazy loading -->

## Full outer joins

- TODO: A full outer join keeps the rows that match and the rows that have no partner on the other side.
- TODO: Use it for a reconciliation that has to show what exists only on the left and what exists only on the right.
- TODO: Assert the SQL text, not only the materialized rows, so a later EF version cannot change the shape unnoticed.
- TODO: Where this product needs that report is [Several collections on one parent](/building-a-saas/07-data-layer/overview#several-collections-on-one-parent).

## Projections

<!-- TODO: Select, anonymous types, DTOs -->

## Filtering and Sorting

<!-- TODO: Where, OrderBy, complex predicates -->

## Pagination

<!-- TODO: Skip, Take, keyset pagination -->

### Offset versus keyset

<!-- TODO -->

### Composite index design

<!-- TODO -->

### Opaque cursor encoding

<!-- TODO -->

### API response shape

<!-- TODO -->

## Raw SQL

<!-- TODO: FromSqlRaw, when to use it -->

## Practical Examples

- See [C#: LINQ](/csharp/advanced-features/linq) - LINQ fundamentals

---

**Next:** [Migrations](/csharp/entity-framework/migrations)
