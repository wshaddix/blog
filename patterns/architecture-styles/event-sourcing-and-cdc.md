# Event Sourcing and Change Data Capture

Two ways a change becomes a stream of facts.

## Event sourcing

## Change data capture

### Reading the log as a relay

- TODO: A consumer can read the database log and publish what committed, instead of polling an outbox table.
- TODO: That reader is a process to run, to watch, and to catch up after it stops. See [Relaying: polling workers vs log-based](/patterns/integration-patterns/outbox-and-idempotent-consumer#relaying-polling-workers-vs-log-based).

## Practical Examples

- See [Building a SaaS: Domain Modeling](/building-a-saas/03-domain-modeling/overview) - Domain events
- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - The audit log

## Related Topics

- See [Choreography and Orchestration](/patterns/integration-patterns/choreography-vs-orchestration)
- See [Outbox and the Idempotent Consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)

---

**Next:** [Distributed Building Blocks](/patterns/architecture-styles/distributed-building-blocks)
