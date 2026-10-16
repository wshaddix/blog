---
title: Failure and Degradation
order: 10
---

# Failure and Degradation

Plan for the failure you did not write a test for.

## Blast radius

- TODO: Name what else stops when this dependency stops.
- TODO: A bulkhead, a queue, or a timeout keeps that circle smaller than the whole request.

## Safe retries

- TODO: Retry a call only when repeating it is safe, or when an idempotency key makes the repeat the same attempt.
- TODO: Add jitter, and stop when the deadline is gone. A timeout is not proof the work failed.

## Degradation

- TODO: Decide the feature you turn off so the rest keeps working.
- TODO: Serving a stale value, or refusing a non-critical action, is a product decision. Write it down.

## Practical Examples

- See [Building a SaaS: Monitoring and Operations](/building-a-saas/12-monitoring-operations/overview) - Degraded modes

## Related Topics

- See [Consistency](/fundamentals/distributed-systems/consistency)
- See [Synchronous call chains](/patterns/integration-patterns/synchronous-call-chains)
- See [HTTP clients](/csharp/platform/http-clients)

---

**Next:** [Chapter 12: Monitoring and Operations](/building-a-saas/12-monitoring-operations/overview)
