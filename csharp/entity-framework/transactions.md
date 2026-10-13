# Transactions

`SaveChanges` is already one transaction. You open your own when more than one save must commit together.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## SaveChanges

One round trip, one transaction, and the failure mode.

## BeginTransaction

Several saves, one commit.

## Execution strategy

A retry that must re-run the whole transaction, not one statement.

## Isolation

The database page is the concept. This page is the API.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Transactions and isolation](/databases/relational/transactions-and-isolation)

---

**Next:** [Performance](/csharp/entity-framework/performance)
