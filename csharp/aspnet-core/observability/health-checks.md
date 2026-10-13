---
title: Health Checks
order: 10
---

# Health Checks

A health endpoint tells a platform whether to send traffic.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Liveness

The process is up.

## Readiness

The process can serve. The database is reachable.

## Checks

A check per dependency, with a timeout.

## What a check must not do

A check that takes a lock or writes a row.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Observability](/csharp/aspnet-core/observability/overview)

---

**Next:** [Observability](/csharp/aspnet-core/observability/overview)
