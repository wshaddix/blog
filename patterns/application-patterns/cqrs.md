# CQRS

Separate the model that changes state from the model that reads it, when those two models want different shapes.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## A command

A request that changes state and returns little.

## A query

A request that returns a shape the screen needs and changes nothing.

## One database, two models

Separate command and query handlers can share one database. The split is in the code.

- TODO: Treat the handler split as a decision about code, independent of where the rows live.
- TODO: Read with `AsNoTracking`, a projection to a DTO, a view, or raw SQL against the same tables the write side uses.
- TODO: Write through aggregates on the tracked context, and keep the invariants there.
- TODO: A separate read store is justified when read load starts to hurt writes, when the queries are shaped like search, or when reporting must retain data longer than the operational tables.
- TODO: A second store means living with lag, keeping a projector running, rebuilding that projector when it falls behind, and migrating two schemas.
- TODO: A read replica is the step between one database and a separate read store. See [Read replicas](/building-a-saas/07-data-layer/overview#read-replicas) and [CQRS without a second store](/building-a-saas/02-architecture-decisions/overview#cqrs-without-a-second-store).

## When it pays

A write model and a read model that have diverged.

## When it does not

A CRUD screen where one model is still honest.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Repository](/patterns/application-patterns/repository)

---

**Next:** [Repository](/patterns/application-patterns/repository)
