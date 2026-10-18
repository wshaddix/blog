# Consistency

Each operation picks how up to date the data has to be.

## One answer

- TODO: A strong read sees the latest committed write. Use it when acting on a stale value would be wrong.
- TODO: That guarantee costs latency and availability when the writers are somewhere else.

## A stale answer

- TODO: A feed, a count, or a cache can lag. Say how far behind is still acceptable.
- TODO: The caller that just wrote may need to read its own write even when everyone else can lag.

## Reading your own writes with replicas

- TODO: The call that just committed can be sent next to a replica that does not have that write yet.
- TODO: Read that follow-up from the primary, or from a replica that has applied the write this caller made.

## Chosen per operation

- TODO: Do not pick one mode for the whole product. The payment and the activity list are different decisions.
- TODO: Write down the choice next to the operation so a later change does not silently strengthen or weaken it.

## Practical Examples

- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview) - Consistency per operation
- See [Building a SaaS: Domain Modeling](/building-a-saas/03-domain-modeling/overview) - Aggregates as a consistency boundary

## Related Topics

- See [Failure and degradation](/fundamentals/distributed-systems/failure-and-degradation)
- See [Transactions and isolation](/databases/relational/transactions-and-isolation)
- See [Transactions](/csharp/entity-framework/transactions)

---

**Next:** [Caching](/fundamentals/distributed-systems/caching)
