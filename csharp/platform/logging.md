---
title: Logging
order: 30
---

# Logging

`ILogger` is the logging abstraction. The sink (console, file, or a vendor) is a registration.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## ILogger

A category, a level, and a message.

## Structured logging

Named placeholders, so a log is data and not only a sentence.

## Scopes

A scope that stamps a request id onto every event inside it.

## Levels

What Trace through Critical are for, and what you leave on in production.

## Where configuration lives

Filters in configuration, not in an `if` around every call.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Observability](/csharp/aspnet-core/observability/overview)
- [Sensitive data in logs](/csharp/security/sensitive-data-in-logs)
- [DevOps logging](/devops/monitoring/logging)

---

**Next:** [HTTP Clients](/csharp/platform/http-clients)
