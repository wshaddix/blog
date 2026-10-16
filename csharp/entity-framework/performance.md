# Entity Framework Performance

Avoiding common performance pitfalls.

## N+1 Query Problem

## Tracking vs No-Tracking

## Compiled Queries

## Batch Operations

## Connection Management

## Profiling

## Where the query actually runs

## Existence checks and counting

## Projections versus loading entities

## Bulk writes

## Reading SQL logs

## Skewed tenant data

- TODO: A database where every tenant has a few rows hides the tenant that has millions.
- TODO: Seed one large tenant and assert the query shape, not only the small case.

## Practical Examples

- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - Performance in practice
- See [Building a SaaS: Testing Strategy](/building-a-saas/10-testing-strategy/overview) - Test data for tenants of different sizes

---

**Continue to:** [ASP.NET Core](/csharp/aspnet-core/web-apis/overview)
