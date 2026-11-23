# Chapter 3: Domain Modeling

The domain model is the heart of your application - getting it right is crucial.

## What We'll Cover

- Domain-Driven Design basics
- Entities vs Value Objects
- Aggregates and aggregate roots
- Domain events
- Our SaaS domain model

## Core Concepts

## Entities

## Value Objects

### Fixed after construction

- TODO: A value object stays as it was built. See [Immutability](/csharp/advanced-features/records#immutability).

## Aggregates

- TODO: Persist an aggregate through EF with a private constructor and a field-backed collection. See [Private setters and backing fields](/csharp/entity-framework/modeling#private-setters-and-backing-fields) and [Collections behind a read-only view](/csharp/entity-framework/modeling#collections-behind-a-read-only-view).

## Our Domain Model

## Domain events

## Aggregate version

## Result-style errors

- TODO: A failure the domain already named can be a union of those cases, instead of a result class.
- TODO: Measure that union before it sits on a hot path. See [Unions on hot paths](/csharp/advanced-features/modern-csharp#unions-on-hot-paths).
- TODO: Each case maps to an HTTP status in [Known failures](/csharp/aspnet-core/web-apis/error-handling#known-failures).

## Related Topics

- See [Fundamentals: OOP Principles](/fundamentals/programming-concepts/oop-principles)
- See [C#: Records](/csharp/advanced-features/records) for value objects
- See [Databases: Data Modeling](/databases/data-modeling/overview)
- See [Event sourcing and change data capture](/patterns/architecture-styles/event-sourcing-and-cdc)

---

**Next:** [Chapter 4: Authentication](/building-a-saas/04-authentication/overview)
