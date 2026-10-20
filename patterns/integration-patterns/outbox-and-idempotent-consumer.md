---
title: Outbox and the Idempotent Consumer
order: 80
---

# Outbox and the Idempotent Consumer

Saving state and sending a message are two writes, and either one can fail on its own.

## The problem: saving state and sending a message are two writes

<!-- TODO: The two writes, and the window between them -->

### Failure timeline walkthrough

<!-- TODO: DB commit ok, publish fails / publish ok, ack lost -->

### Why "exactly-once" is really at-least-once plus dedup

<!-- TODO: What you can actually promise -->

## When you can skip it

- TODO: Skip a separate outbox when the state change is the only write, and no other system has to learn that it happened.
- TODO: Skip it when a missed message is acceptable and a later successful write repairs the gap.
- TODO: Use the outbox when another system must observe the change, and a crash between the save and the send would drop that fact.

## Transactional outbox

<!-- TODO: Write the message in the same transaction as the state change -->

### OutboxMessages table schema

<!-- TODO: EF Core entity and configuration -->

### Writing to the outbox inside SaveChanges

<!-- TODO: Interceptor converting domain events -->

### Dispatcher

<!-- TODO: BackgroundService vs Hangfire recurring job; batching and locking (UPDLOCK, READPAST) -->

### PostgreSQL claim query

- TODO: Claim a batch by taking only rows that are still unpublished, and leave rows another worker has already claimed.
- TODO: On PostgreSQL the claim is one statement that locks the chosen rows and returns them. A second worker's claim returns a different batch.

### Cleanup and retention

<!-- TODO: How long outbox rows stay -->

## Idempotent consumer

<!-- TODO: Handle a message that arrives more than once -->

### Natural idempotency vs tracked idempotency

<!-- TODO: Decision table -->

### ProcessedMessages table

<!-- TODO: Unique (MessageId, Handler) key -->

### Idempotency keys for outbound calls

<!-- TODO: Stripe, email -->

## Testing it

<!-- TODO: Simulate a crash between commit and publish with an integration test -->

## In the SaaS app

<!-- TODO: Chapter 8 publishes through the outbox; Chapter 9 handles webhooks -->

## Practical Examples

- See [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview) - Reliable messaging
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview) - Webhook handler

## Related Topics

- See [Chapter 3: Domain Modeling](/building-a-saas/03-domain-modeling/overview) - Domain events
- See [Background Services](/csharp/aspnet-core/web-apis/background-services)
- See [Sagas](/patterns/integration-patterns/sagas)

---

**Next:** [Sagas](/patterns/integration-patterns/sagas)
