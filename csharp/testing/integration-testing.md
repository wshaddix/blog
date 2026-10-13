# Integration Testing

An integration test checks that two or more real parts work together. On this site that usually means the API, the database, or both. The runner is still TUnit.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## What it proves

A request reaches a handler, the handler talks to a real database or a real HTTP boundary, and the status and body match the contract. It does not replace the unit tests around the domain rules.

## ASP.NET Core

Boot the app in-process with `TUnit.AspNetCore`. The factory, the test base class, and per-test isolation are on the [ASP.NET Core tests](/csharp/testing/webapplicationfactory) page.

## Databases

Use SQLite when you need a relational engine and the SQL is ordinary. Use [Testcontainers](/csharp/testing/testcontainers) when the behavior is SQL Server-specific. Do not use the EF in-memory provider to stand in for either one.

## Parallelism

TUnit runs tests in parallel. Give each test its own database, or mark the class `[NotInParallel]` when the tests share one.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Testing strategy](/sdlc/testing-strategy)
- [Testing Entity Framework](/csharp/entity-framework/testing)
- [Building a SaaS: Testing](/building-a-saas/10-testing-strategy/overview)

---

**Next:** [ASP.NET Core Tests](/csharp/testing/webapplicationfactory)
