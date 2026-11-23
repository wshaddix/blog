# Outbox and the Idempotent Consumer

Saving state and sending a message are two writes, and either one can fail on its own.

## The problem: saving state and sending a message are two writes

### Failure timeline walkthrough

### Why "exactly-once" is really at-least-once plus dedup

## When you can skip it

- TODO: Skip a separate outbox when the state change is the only write, and no other system has to learn that it happened.
- TODO: Skip it when a missed message is acceptable and a later successful write repairs the gap.
- TODO: Use the outbox when another system must observe the change, and a crash between the save and the send would drop that fact.

## Transactional outbox

### OutboxMessages table schema

### Writing to the outbox inside SaveChanges

### Dispatcher

### PostgreSQL claim query

- TODO: Claim a batch by taking only rows that are still unpublished, and leave rows another worker has already claimed.
- TODO: On PostgreSQL the claim is one statement that locks the chosen rows and returns them. A second worker's claim returns a different batch.

### Cleanup and retention

## Relaying: polling workers vs log-based

- TODO: The relay keeps order for one aggregate, and it delivers at least once.
- TODO: Several pollers can run at once. A claim takes a row for one of them, so two workers do not send the same message.
- TODO: Reading the database change log skips the poll. That reader is another process to operate.
- TODO: Pick the poll or the log from the throughput you need and from who can run the extra process.
- TODO: The log side is [Reading the log as a relay](/patterns/architecture-styles/event-sourcing-and-cdc#reading-the-log-as-a-relay). How this product relays is [How the outbox leaves the database](/building-a-saas/08-background-jobs/overview#how-the-outbox-leaves-the-database).

## Idempotent consumer

### Natural idempotency vs tracked idempotency

### ProcessedMessages table

### Idempotency keys for outbound calls

## Testing it

## In the SaaS app

## Practical Examples

- See [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview) - Reliable messaging
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview) - Webhook handler

## Related Topics

- See [Chapter 3: Domain Modeling](/building-a-saas/03-domain-modeling/overview) - Domain events
- See [Background Services](/csharp/aspnet-core/web-apis/background-services)
- See [Message brokers](/patterns/integration-patterns/message-brokers)
- See [Sagas](/patterns/integration-patterns/sagas)

---

**Next:** [Sagas](/patterns/integration-patterns/sagas)
