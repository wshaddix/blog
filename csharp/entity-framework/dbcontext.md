# DbContext

The central class for database interaction in EF Core.

## DbContext Lifecycle

## DbSet<T>

## Configuration

## Change Tracking

## SaveChanges

## A context in a background worker

- TODO: A context tied to one request is gone when that request ends, and two threads cannot share it.
- TODO: The worker opens a scope for the job, resolves a new context inside that scope, and disposes the scope when the job ends.

## Practical Examples

- See [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview) - A context in a background worker

## Related Topics

- See [Background services](/csharp/aspnet-core/web-apis/background-services)

---

**Next:** [Querying](/csharp/entity-framework/querying)
