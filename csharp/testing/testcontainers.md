---
title: Testcontainers
order: 50
---

# Testcontainers

A test can start a real SQL Server in Docker and throw it away when the test session ends.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## When

Behavior that SQLite does not match: types, full-text, or a SQL Server-only feature.

## The fixture

A container started once per session through a TUnit `[ClassDataSource]`, and disposed at the end.

## The connection string

Point the `TestWebApplicationFactory` at the container.

## Migrations

Apply the model to the empty database. Do not point the test at a shared server.

## Local requirement

Docker has to be running. Say so in the test project's readme.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Testing Entity Framework](/csharp/entity-framework/testing)
- [ASP.NET Core tests](/csharp/testing/webapplicationfactory)

---

**Next:** [bUnit](/csharp/testing/bunit)
