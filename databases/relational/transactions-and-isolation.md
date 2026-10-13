# Transactions and Isolation

How a group of writes becomes one atomic change, and the anomalies each isolation level allows.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Atomicity

Commit and rollback. A failure halfway through.

## Isolation levels

Read committed, snapshot, and serializable. What each one prevents.

## Anomalies

Dirty reads, non-repeatable reads, and phantoms.

## Deadlocks

Two transactions waiting on each other, and how the engine picks a victim.

## In application code

A transaction around more than one `SaveChanges`, and the length of the lock.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Entity Framework transactions](/csharp/entity-framework/transactions)

---

**Next:** [Indexes and Query Plans](/databases/relational/indexes-and-query-plans)
