---
title: Idempotent Requests
order: 210
---

# Idempotent Requests

A client that retries a POST needs the server to recognize the same attempt.

## The Idempotency-Key

<!-- TODO: A caller-generated key sent on the request -->

### Where it is stored

<!-- TODO: Persist the key with the status code and the response body -->

## The first request

<!-- TODO: Run the operation once and store the outcome under the key -->

## A retry of the same request

<!-- TODO: Return the stored response. The operation stays as it was after the first success -->

## The same key with a different body

<!-- TODO: Reject the call. The key already identifies another payload -->

## A key whose request is still running

<!-- TODO: A second request arrives before the first has stored an outcome -->

## How long the outcome is kept

<!-- TODO: Retention, and a key that is presented again after the record expires -->

## Inbound and outbound

<!-- TODO: This page is the key on requests the API receives. Outbound keys travel on HttpClient calls -->

## Practical Examples

- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview) - Idempotency-Key on commands the client may retry
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview) - Idempotency keys on calls the app sends

## Related Topics

- See [HTTP and the Web](/fundamentals/networking/http)
- See [HTTP clients](/csharp/platform/http-clients)
- See [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)

---

**Next:** [Minimal APIs and Controllers](/csharp/aspnet-core/web-apis/minimal-apis-and-controllers)
