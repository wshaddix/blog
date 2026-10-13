# ASP.NET Core Tests

API tests boot the app in-process with `TUnit.AspNetCore`. Use `TestWebApplicationFactory<TEntryPoint>`, not the vanilla `WebApplicationFactory<T>`, so traces and logs stay tied to the test that made the call.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The package

`TUnit.AspNetCore`.

## The factory

A `TestWebApplicationFactory<TEntryPoint>` that replaces the database and any external client.

## The test base

`WebApplicationTest<TFactory, TEntryPoint>` so each test gets an isolated client.

## Arrange the app

Swap the real database and downstream HTTP clients for test doubles or containers.

## Call the endpoint

An `HttpClient` from the factory, then `Assert.That` on the status and the body.

## Parallelism

Tests run in parallel. A shared database needs a per-test database name or `[NotInParallel]`.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Integration testing](/csharp/testing/integration-testing)
- [Testcontainers](/csharp/testing/testcontainers)
- [Health checks](/csharp/aspnet-core/observability/health-checks)

---

**Next:** [Testcontainers](/csharp/testing/testcontainers)
