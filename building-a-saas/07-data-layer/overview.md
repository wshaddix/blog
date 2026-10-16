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

## HybridCache

## Audit logging

## File storage

- TODO: Keep file bytes in blob storage. Keep the blob name, content type, and owner on the tenant row.
- TODO: Use a conditional write so a retry does not replace an object another request already stored.

## Related Topics

- See [Entity Framework](/csharp/entity-framework/getting-started)
- See [Entity Framework performance](/csharp/entity-framework/performance)
- See [Concurrency](/csharp/entity-framework/concurrency)
- See [Caching](/csharp/aspnet-core/web-apis/caching)
- See [Databases](/databases/overview)
- See [Blob Storage](/devops/azure/blob-storage)

---

**Next:** [Chapter 8: Background Jobs](/building-a-saas/08-background-jobs/overview)
