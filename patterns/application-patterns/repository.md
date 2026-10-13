---
title: Repository
order: 50
---

# Repository

A repository is a collection-shaped front for one aggregate. `DbContext` is already a unit of work, so a second unit-of-work wrapper needs a reason.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The shape

Get, add, and a query method that says what it returns.

## What it hides

The ORM, so a domain service does not take a `DbContext` it can use for anything.

## What it must not hide

A query the caller has to compose. That caller should be in the data project.

## Unit of work

One context, one `SaveChanges`, one transaction. A custom unit of work when a use case spans two contexts.

## The catalog

Fowler's catalog lists many persistence patterns. This page is the one this path teaches.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [DbContext](/csharp/entity-framework/dbcontext)
- [Application pattern catalog](/patterns/application-patterns/overview)

---

**Next:** [CQRS](/patterns/application-patterns/cqrs)
