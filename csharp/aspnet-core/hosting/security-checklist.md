---
title: Security Checklist
order: 20
---

# Security Checklist

Each category on the current top-ten risk list points at the page on this site that covers it.

## Access to an action

- TODO: Who may perform an action is [Permission-based authorization](/csharp/aspnet-core/authorization/permissions).
- TODO: Whether this row is in scope is [Resource-based authorization](/csharp/aspnet-core/authorization/resource-based).

## Access to a tenant's rows

- TODO: The application filter is [Data isolation](/building-a-saas/05-multi-tenancy/overview#data-isolation).
- TODO: The database rule under that filter is [Row-level security](/databases/relational/row-level-security).

## Sign-in

- TODO: How a caller proves who they are is [Authentication](/csharp/aspnet-core/authentication/overview).
- TODO: Lifetime and revocation of a bearer token are [JWT bearer](/csharp/aspnet-core/authentication/jwt).

## Secrets and transport

- TODO: Where secrets live is [Secrets](/csharp/security/secrets).
- TODO: HTTPS and response headers are [Transport and headers](/csharp/security/transport-and-headers) and [Kestrel and HTTPS](/csharp/aspnet-core/hosting/kestrel-and-https).

## Untrusted input

- TODO: Reject a body that cannot succeed in [Validation](/csharp/aspnet-core/web-apis/validation).
- TODO: Queries go through the model. Hand-written SQL is [Raw SQL](/csharp/entity-framework/raw-sql).

## Components you did not write

- TODO: Pin the actions a workflow runs. See [Pinning actions](/devops/ci-cd/github-actions#pinning-actions).
- TODO: A runtime that is no longer serviced is [Support windows and end of support](/csharp/platform/publishing#support-windows-and-end-of-support).

## Failures and logs

- TODO: An error body that hides internals is [Unknown failures](/csharp/aspnet-core/web-apis/error-handling#unknown-failures).
- TODO: Logs that omit secrets are [Sensitive data in logs](/csharp/security/sensitive-data-in-logs).
- TODO: Knowing that a failure happened is [Alerting](/devops/monitoring/alerting).

## An address the caller supplied

- TODO: Check a webhook URL before the request is sent. See [Outgoing webhooks for tenants](/building-a-saas/06-api-development/overview#outgoing-webhooks-for-tenants).

## Line the list up

- TODO: Before this page is treated as finished, match each bullet to the current top-ten list and add any category this index still skips.
- TODO: The walkthrough for sign-in and for tenant data is [Closing checklist](/building-a-saas/04-authentication/overview#closing-checklist) and [Closing checklist](/building-a-saas/05-multi-tenancy/overview#closing-checklist).

## Related Topics

- See [Kestrel and HTTPS](/csharp/aspnet-core/hosting/kestrel-and-https)
- See [Security](/csharp/security/overview)
- See [Building a SaaS: Authentication](/building-a-saas/04-authentication/overview)
- See [Building a SaaS: Multi-Tenancy](/building-a-saas/05-multi-tenancy/overview)

---

**Next:** [Kestrel and HTTPS](/csharp/aspnet-core/hosting/kestrel-and-https)
