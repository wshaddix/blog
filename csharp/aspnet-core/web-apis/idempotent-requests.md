# Idempotent Requests

A client that retries a POST needs the server to recognize the same attempt.

## The Idempotency-Key

### Where it is stored

### Same transaction as the work

- TODO: Commit the stored outcome in the same transaction as the work it describes.
- TODO: The order and its outcome land together, so a retry has one result to return.

## The first request

## A retry of the same request

## The same key with a different body

## A key whose request is still running

### Claiming the key in one statement

- TODO: Claim the key with one insert. A unique constraint makes a second insert lose, so only one request becomes the first.
- TODO: While the claim is open and no outcome is stored, the request that loses receives 409 and leaves the work untouched.

### Scope per tenant

- TODO: Include the tenant in the unique index. The same key string from another tenant is a different request.

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

**Next:** [Webhooks](/csharp/aspnet-core/web-apis/webhooks)
