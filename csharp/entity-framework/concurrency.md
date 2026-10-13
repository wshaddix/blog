---
title: Concurrency
order: 45
---

# Concurrency Control in EF Core

How two saves of the same row avoid a lost update.

## Lost update, illustrated

<!-- TODO: Two readers, two writers, one silent overwrite -->

## Optimistic concurrency

<!-- TODO: rowversion and concurrency tokens, handling DbUpdateConcurrencyException, returning 409/412 with ETags -->

## Pessimistic concurrency

<!-- TODO: SQL Server lock hints, and when a lock is justified -->

## Atomic updates with ExecuteUpdate

<!-- TODO: Counters and seat limits -->

## Decision table

<!-- TODO: Optimistic, pessimistic, or an atomic update -->

## In the SaaS app

<!-- TODO: Subscription seats and plan changes -->

## Practical Examples

- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview) - Seats and plan changes
- See [Building a SaaS: Domain Modeling](/building-a-saas/03-domain-modeling/overview) - Aggregate version

## Related Topics

- See [Transactions](/csharp/entity-framework/transactions)
- See [Transactions and Isolation](/databases/relational/transactions-and-isolation)

---

**Next:** [Performance](/csharp/entity-framework/performance)
