# Repository

A repository is a collection-shaped front for one aggregate. `DbContext` is already a unit of work, so a second unit-of-work wrapper needs a reason.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The shape

Get, add, and a query method that says what it returns.

## What it hides

The ORM, so a domain service does not take a `DbContext` it can use for anything.

## What it must not hide

A query the caller has to compose. That caller should be in the data project.

## A generic repository over EF Core

A generic type that only forwards calls to EF Core is an extra interface in front of the one you already have.

- TODO: Remember what `DbSet<T>` and `DbContext` already are: a repository, and a unit of work.
- TODO: On a pass-through `IRepository<T>`, Get, Add, Update, and Delete each forward one call to EF and then stop.
- TODO: That wrapper either lets `IQueryable` leak out or wraps it again, drops includes and projections, and gives tests another interface to mock.
- TODO: A repository earns the extra type when it enforces a rule: tenant scope, soft delete, how an aggregate is loaded, or a named query.
- TODO: Write that type for one aggregate. One generic repository for every entity does not name a rule.
- TODO: The decision test is to name the rule. With no rule to name, call the context. How this product applies that test is [What a wrapper would have to enforce](/building-a-saas/07-data-layer/overview#what-a-wrapper-would-have-to-enforce).

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
