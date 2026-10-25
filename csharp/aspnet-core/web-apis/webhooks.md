# Webhooks

An HTTP callback the app receives, or sends, when something has already happened.

## Verifying a signature

- TODO: Compute the signature over the raw body bytes, before a parser rewrites the payload.
- TODO: Compare the computed signature to the header in constant time.
- TODO: Reject a timestamp outside a short window so a captured call cannot be submitted again later.

## A secret per subscriber

- TODO: Give each subscriber its own signing secret.
- TODO: Rotating one subscriber's secret leaves every other subscriber's secret in place.

## Tenant callback URLs

- TODO: A tenant-supplied URL is an outbound request. Resolve it and refuse a loopback, link-local, private, or metadata address.
- TODO: Run that check again when a redirect would send the request to a different host.

## Replaying a failed delivery

- TODO: Store each delivery and its outcome. Retry a failure with the same event identity so the receiver can treat the replay as a duplicate.
- TODO: Stop after a bounded number of attempts and leave the failed delivery recorded.

## Practical Examples

- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview) - Outgoing webhooks for tenants
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview) - Inbound subscription webhooks

## Related Topics

- See [Idempotent requests](/csharp/aspnet-core/web-apis/idempotent-requests)
- See [HTTP clients](/csharp/platform/http-clients)

---

**Next:** [Conditional Requests](/csharp/aspnet-core/web-apis/conditional-requests)
