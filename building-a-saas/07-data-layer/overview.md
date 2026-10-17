---
title: Overview
order: 1
---

# Chapter 7: Data Layer

The data layer connects your domain model to the database. Done right, it's reliable and performant.

## What We'll Cover

- Entity Framework Core configuration
- Entity configurations (Fluent API)
- Migrations strategy
- Repository pattern (or not?)
- Query optimization
- Audit logging

## DbContext Setup

<!-- TODO: Configuration, connection strings -->

## Entity Configurations

<!-- TODO: Fluent API, relationships, indexes -->

## Migrations

<!-- TODO: Creating, applying, CI/CD integration -->

## Repository Pattern?

<!-- TODO: When to use, when DbContext is enough -->

## Performance

<!-- TODO: N+1, tracking, projections, keyset pagination -->

## HybridCache

<!-- TODO: Tenant settings and plan lookups, keyed by tenant -->

## Audit logging

<!-- TODO: A record of changes for the tenant -->

## File storage

- TODO: Keep file bytes in blob storage. Keep the blob name, content type, and owner on the tenant row.
- TODO: Use a conditional write so a retry does not replace an object another request already stored.

## Schemas per module

- TODO: Give each module its own schema and its own `DbContext`.
- TODO: Keep a module's queries inside its context. A join across those schemas belongs in a report.

## Related Topics

- See [Modular monolith](/patterns/architecture-styles/modular-monolith)
- See [Entity Framework](/csharp/entity-framework/getting-started)
- See [Entity Framework performance](/csharp/entity-framework/performance)
- See [Concurrency](/csharp/entity-framework/concurrency)
- See [Caching](/csharp/aspnet-core/web-apis/caching)
- See [Databases](/databases/overview)
- See [Blob Storage](/devops/azure/blob-storage)

---

**Next:** [Chapter 8: Background Jobs](/building-a-saas/08-background-jobs/overview)
