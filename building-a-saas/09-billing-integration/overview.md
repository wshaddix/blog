---
title: Overview
order: 1
---

# Chapter 9: Billing Integration

Monetization is what makes a SaaS sustainable. We'll integrate Stripe for subscription billing.

## What We'll Cover

- Stripe setup and concepts
- Products and prices
- Subscription lifecycle
- Webhook handling
- Customer portal
- Usage-based billing considerations

## Stripe Concepts

| Concept | Description |
|---------|-------------|
| Customer | Your tenant/user |
| Product | What you're selling |
| Price | How much and how often |
| Subscription | Ongoing relationship |
| Invoice | Payment record |

## Implementation

<!-- TODO: Stripe.NET SDK, checkout flow -->

## Webhooks

<!-- TODO: Subscription events, idempotency -->

## Subscription Management

<!-- TODO: Upgrades, downgrades, cancellation -->

## Trial Periods

<!-- TODO: Free trials, conversion, and a clock tests can control -->

## Usage-based billing

<!-- TODO: Meter product usage for usage-based prices -->

## Resilient outbound calls

<!-- TODO: Stripe client and email provider: timeouts, retries, and idempotency keys -->

## Concurrency for seats and plan changes

<!-- TODO: Lost updates on seat counts and plan changes -->

## Related Topics

- See [Concurrency](/csharp/entity-framework/concurrency)
- See [HTTP clients](/csharp/platform/http-clients)
- See [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)

---

**Next:** [Chapter 10: Testing Strategy](/building-a-saas/10-testing-strategy/overview)
