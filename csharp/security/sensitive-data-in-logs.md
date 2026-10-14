---
title: Sensitive Data in Logs
order: 25
---

# Sensitive Data in Logs

A value written to a log is copied into every sink that stores that log.

## Values that stay out of logs

<!-- TODO: Passwords, tokens, connection strings, payment data, and government identifiers -->

## Classification

<!-- TODO: Mark properties the logger should treat as secrets or personal data -->

## Redaction

<!-- TODO: Register a redactor so the value is masked before any sink receives it -->

### Erasing and hashing

<!-- TODO: Remove the value, or replace it with a stable hash when correlation still matters -->

## Message templates

<!-- TODO: Named placeholders so the redactor can see the argument -->

## What the event still contains

<!-- TODO: A correlation id and the operation, with the secret removed -->

## Environments

<!-- TODO: Production redacts the classified fields. Development can keep a narrower set visible -->

## Practical Examples

- See [Building a SaaS: Monitoring](/building-a-saas/12-monitoring-operations/overview) - Redaction before events leave the process

## Related Topics

- See [Logging](/csharp/platform/logging)
- See [Secrets](/csharp/security/secrets)
- See [DevOps: Logging](/devops/monitoring/logging)

---

**Next:** [Transport and Headers](/csharp/security/transport-and-headers)
