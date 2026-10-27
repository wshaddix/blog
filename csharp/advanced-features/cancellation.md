---
title: Cancellation
order: 45
---

# Cancellation

Cooperative cancellation, and a limit on how much work runs at once.

## Cancellation

<!-- TODO: CancellationToken, linking tokens, and honoring the token through the call stack -->

### Request timeouts

<!-- TODO: A request timeout and the token the work receives. See [Request timeouts](/building-a-saas/06-api-development/overview#request-timeouts). -->

### Work that must not be cancelled

<!-- TODO: Work that still runs after the client disconnects. See [A charge that outlives the request](/building-a-saas/09-billing-integration/overview#a-charge-that-outlives-the-request). -->

## Bounded concurrency

<!-- TODO: A cap on parallel work -->

## Practical Examples

- See [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview) - Shutdown
- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview#request-timeouts) - Request timeouts
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview) - Refunds
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview#a-charge-that-outlives-the-request) - A charge that outlives the request

## Related Topics

- See [Async/Await](/csharp/advanced-features/async)
- See [Background Services](/csharp/aspnet-core/web-apis/background-services)

---

**Next:** [Records](/csharp/advanced-features/records)
