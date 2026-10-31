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

### Status values a person can read

A status stored on an entity should be readable in a query without a decoder.

- TODO: Prefer a name, a string conversion, or a lookup row over a bare integer for a status a person will read.
- TODO: Guard the allowed set, and plan how a renamed or retired value is migrated. See [Text, number, or lookup table](/csharp/entity-framework/modeling#text-number-or-lookup-table).

## Migrations

## Repository Pattern?

## Performance

### Latest activity per project

- TODO: The dashboard query that returns the newest item for each parent row is served by the column order in [Equality columns then the sort](/databases/relational/indexes-and-query-plans#equality-columns-then-the-sort).

### Narrow locks

- TODO: Lock the row or the key this operation changes, so unrelated work does not wait. See [Lock granularity](/fundamentals/programming-concepts/concurrency#lock-granularity) and [Concurrency](/csharp/entity-framework/concurrency).

### Fan-out and the connection pool

A fan-out that opens one database call per item can take every connection the pool has.

- TODO: Cap how many of those calls run together so other requests can still borrow a connection.
- TODO: Size the cap from the pool, and cancel the rest of the fan-out when one call fails. See [Starting too many at once](/fundamentals/programming-concepts/concurrency#starting-too-many-at-once).

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

### Reusing model answers

- TODO: A repeated question can reuse a stored model answer. See [Reusing answers to similar questions](/csharp/mcp/clients-and-agents#reusing-answers-to-similar-questions).

### Not-found results

- TODO: A lookup that finds nothing can be stored as an entry. See [Empty results](/csharp/aspnet-core/web-apis/caching#empty-results).

## Audit logging

## File storage

- TODO: Keep file bytes in blob storage. Keep the blob name, content type, and owner on the tenant row.
- TODO: Use a conditional write so a retry does not replace an object another request already stored.

### Files an agent reads

- TODO: Give the agent the blob name and the metadata, and read the bytes on a later call only when the turn needs them. See [Return a reference, not the bytes](/csharp/mcp/clients-and-agents#return-a-reference-not-the-bytes).

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
