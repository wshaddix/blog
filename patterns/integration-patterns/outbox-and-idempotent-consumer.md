# Outbox and the Idempotent Consumer

Saving state and sending a message are two writes, and either one can fail on its own.

## The problem: saving state and sending a message are two writes

### Failure timeline walkthrough

### Why "exactly-once" is really at-least-once plus dedup

## Transactional outbox

### OutboxMessages table schema

### Writing to the outbox inside SaveChanges

### Dispatcher

### Cleanup and retention

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
- See [Sagas](/patterns/integration-patterns/sagas)

---

**Next:** [Sagas](/patterns/integration-patterns/sagas)
