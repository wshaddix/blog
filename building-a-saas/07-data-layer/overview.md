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

## Large ID lists

- TODO: A bulk check or an export can pass thousands of ids into one query.
- TODO: Join to that set. Do not run one query per id.

## SaveChanges in a loop

- TODO: An import that saves every row commits once per row, or holds one transaction for the whole batch.
- TODO: Save at the end of the batch, and do not retry rows that already committed when one row fails.

## HybridCache

<!-- TODO: Tenant settings and plan lookups, keyed by tenant -->

### Local copies across servers

- TODO: Each instance keeps a local copy of a tenant setting in front of the shared cache.
- TODO: After that setting changes, another instance can still serve its local copy until the copy expires.

## Audit logging

<!-- TODO: A record of changes for the tenant -->

## File storage

- TODO: Keep file bytes in blob storage. Keep the blob name, content type, and owner on the tenant row.
- TODO: Use a conditional write so a retry does not replace an object another request already stored.

## Schemas per module

- TODO: Give each module its own schema and its own `DbContext`.
- TODO: Keep a module's queries inside its context. A join across those schemas belongs in a report.

### A connection string per module

- TODO: Point each module's `DbContext` at its own connection string and its own database login.
- TODO: Grant that login the module's schema only, so the database enforces the boundary in [A login per module](/patterns/architecture-styles/modular-monolith#a-login-per-module).
- TODO: A module that opens another module's connection string can see tables it does not own. Do not share the string.

## Read replicas

- TODO: A read that is allowed to lag can use a replica. A follow-up read of a write this caller just made follows [Reading your own writes with replicas](/fundamentals/distributed-systems/consistency#reading-your-own-writes-with-replicas).
- TODO: Send that follow-up to the primary, or to a replica that has applied the write.

## Related Topics

- See [Modular monolith](/patterns/architecture-styles/modular-monolith)
- See [Entity Framework](/csharp/entity-framework/getting-started)
- See [Entity Framework performance](/csharp/entity-framework/performance)
- See [Concurrency](/csharp/entity-framework/concurrency)
- See [Caching](/csharp/aspnet-core/web-apis/caching)
- See [Caching fundamentals](/fundamentals/distributed-systems/caching)
- See [Databases](/databases/overview)
- See [Consistency](/fundamentals/distributed-systems/consistency)
- See [Distributed building blocks](/patterns/architecture-styles/distributed-building-blocks)
- See [Blob Storage](/devops/azure/blob-storage)

---

**Next:** [Chapter 8: Background Jobs](/building-a-saas/08-background-jobs/overview)
