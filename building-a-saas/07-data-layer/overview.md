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

## Entity Configurations

## Migrations

## Repository Pattern?

## Performance

## Large ID lists

- TODO: A bulk check or an export can pass thousands of ids into one query.
- TODO: Join to that set. Do not run one query per id.

## SaveChanges in a loop

- TODO: An import that saves every row commits once per row, or holds one transaction for the whole batch.
- TODO: Save at the end of the batch, and do not retry rows that already committed when one row fails.

## HybridCache

### Local copies across servers

- TODO: Each instance keeps a local copy of a tenant setting in front of the shared cache.
- TODO: After that setting changes, another instance can still serve its local copy until the copy expires.

## Audit logging

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
- See [Caching fundamentals](/fundamentals/distributed-systems/caching)
- See [Databases](/databases/overview)
- See [Blob Storage](/devops/azure/blob-storage)

---

**Next:** [Chapter 8: Background Jobs](/building-a-saas/08-background-jobs/overview)
