# Dependency Injection

A type asks for what it needs. The container creates it.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Registration

`AddSingleton`, `AddScoped`, and `AddTransient`.

## Lifetimes

One instance for the process, one for a scope, or one per request.

## Captive dependencies

A singleton that takes a scoped service.

## Keyed services

More than one implementation of the same interface.

## Composition root

Registration happens at startup. Service location does not spread through the app.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Generic host](/csharp/platform/generic-host)

---

**Next:** [Configuration and Options](/csharp/platform/configuration-and-options)
