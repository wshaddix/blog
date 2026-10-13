---
title: Configuration and Options
order: 40
---

# Configuration and Options

Settings come from files, environment variables, and user secrets. Code reads them through the options pattern.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Sources

`appsettings.json`, environment-specific files, environment variables, and command-line args.

## Environments

Which file is loaded, and what must differ between machines.

## User secrets

A developer secret that never goes in the project file.

## IOptions

`IOptions`, `IOptionsSnapshot`, and `IOptionsMonitor`.

## Validation

Fail at startup when a required setting is missing.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Secrets](/csharp/security/secrets)
- [Generic host](/csharp/platform/generic-host)

---

**Next:** [Logging](/csharp/platform/logging)
