---
title: Overview
order: 1
---

# Chapter 3: Domain Modeling

The domain model is the heart of your application - getting it right is crucial.

## What We'll Cover

- Domain-Driven Design basics
- Entities vs Value Objects
- Aggregates and aggregate roots
- Domain events
- Our SaaS domain model

## Core Concepts

<!-- TODO: Ubiquitous language, bounded contexts -->

## Entities

<!-- TODO: Identity, lifecycle, examples -->

## Value Objects

<!-- TODO: Immutability, equality, examples -->

### Fixed after construction

- TODO: A value object stays as it was built. See [Immutability](/csharp/advanced-features/records#immutability).

## Aggregates

<!-- TODO: Consistency boundaries, aggregate roots -->

## Our Domain Model

<!-- TODO: Tenant, User, Subscription, etc. -->

## Domain events

<!-- TODO: Events inside the model, and why they are not the public API -->

## Aggregate version

<!-- TODO: rowversion on the aggregate -->

## Related Topics

- See [Fundamentals: OOP Principles](/fundamentals/programming-concepts/oop-principles)
- See [C#: Records](/csharp/advanced-features/records) for value objects
- See [Databases: Data Modeling](/databases/data-modeling/overview)
- See [Event sourcing and change data capture](/patterns/architecture-styles/event-sourcing-and-cdc)

---

**Next:** [Chapter 4: Authentication](/building-a-saas/04-authentication/overview)
