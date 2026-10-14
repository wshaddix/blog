# Idempotent Requests

A client that retries a POST needs the server to recognize the same attempt.

## The Idempotency-Key

### Where it is stored

## The first request

## A retry of the same request

## The same key with a different body

## A key whose request is still running

## How long the outcome is kept

## Inbound and outbound

## Practical Examples

- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview) - Idempotency-Key on commands the client may retry
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview) - Idempotency keys on calls the app sends

## Related Topics

- See [HTTP and the Web](/fundamentals/networking/http)
- See [HTTP clients](/csharp/platform/http-clients)
- See [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)

---

**Next:** [Minimal APIs and Controllers](/csharp/aspnet-core/web-apis/minimal-apis-and-controllers)
