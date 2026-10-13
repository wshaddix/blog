---
title: The .NET Platform
order: 70
---

# The .NET Platform

Console apps, MCP servers, APIs, Blazor, WinUI, and Uno are composed the same way: a host, a service container, configuration, and logging.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## In this section

- [Generic host](/csharp/platform/generic-host) - The process model every app type starts from.
- [Dependency injection](/csharp/platform/dependency-injection) - Registration and lifetimes.
- [Configuration and options](/csharp/platform/configuration-and-options) - Settings, environments, and the options pattern.
- [Logging](/csharp/platform/logging) - `ILogger` and structured events.
- [HTTP clients](/csharp/platform/http-clients) - Typed clients, timeouts, and retries.
- [Publishing](/csharp/platform/publishing) - How a build becomes something you can run.

## One composition model

Build the host, register services, then run.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Generic host](/csharp/platform/generic-host)

---

**Next:** [Generic Host](/csharp/platform/generic-host)
