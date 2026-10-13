---
title: Testing Entity Framework
order: 10
---

# Testing Entity Framework

Test against a relational database. The in-memory provider does not enforce the constraints your production database enforces.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## SQLite

A fast relational stand-in for unit-style tests of queries.

## SQL Server

Testcontainers when the behavior is SQL Server-specific.

## A context per test

Isolation under TUnit's default parallelism.

## What you assert

The rows, not the number of times a mock repository was called.

## Migrations

Tests apply the model. They do not share a developer's database.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [TUnit project setup](/csharp/testing/project-setup)
- [Testcontainers](/csharp/testing/testcontainers)

---

**Next:** [Getting Started](/csharp/entity-framework/getting-started)
