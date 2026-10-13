---
title: Generic Host
order: 60
---

# Generic Host

The host builds configuration, the service provider, and logging, then runs until it is stopped.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## CreateApplicationBuilder

The entry point for a console app and for a worker.

## WebApplicationBuilder

The same host, plus Kestrel and the HTTP pipeline.

## Hosted services

`IHostedService` and `BackgroundService`.

## Lifetime

Starting, stopping, and `IHostApplicationLifetime`.

## Environments

Development, Staging, and Production as host environments.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Dependency injection](/csharp/platform/dependency-injection)
- [Console apps](/csharp/console/overview)

---

**Next:** [.NET Aspire](/csharp/platform/aspire)
