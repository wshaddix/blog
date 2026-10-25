# Transactions and Isolation

How a group of writes becomes one atomic change, and the anomalies each isolation level allows.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Atomicity

Commit and rollback. A failure halfway through.

## Isolation levels

Read committed, snapshot, and serializable. What each one prevents.

## Anomalies

Dirty reads, non-repeatable reads, and phantoms.

### Two inserts that both pass a check

- TODO: Two transactions each read "no overlap", and each inserts its own row. No row was updated twice, so a row version catches nothing.
- TODO: Make the save fail for the second one: a unique or exclusion constraint, an update to a shared parent row that carries a version, or serializable isolation.
- TODO: Pick the constraint when the rule fits one. Pick the parent row when the rule is a count.

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
