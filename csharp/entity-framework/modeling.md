---
title: Modeling
order: 90
---

# Modeling

How a C# model becomes tables. Conventions first, then Fluent API where a convention is wrong.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Entities and keys

A key, a generated value, and a type that is not an entity.

## Relationships

One-to-many and many-to-many. Required and optional.

## Owned types

A value object stored in the owner's table.

## Conversions

An enum, a strongly typed id, and a value the database stores as a primitive.

### Text, number, or lookup table

A status is read by people in queries and tickets, so the stored form has to carry its meaning.

- TODO: Show what a bare integer hides from someone looking at the row without the application.
- TODO: Store an enum as its name through a value conversion, so the column reads as text.
- TODO: Hold the allowed values in a lookup table and point each row at one with a foreign key.
- TODO: Add a CHECK constraint so a write outside that set fails in the database.
- TODO: Cover renaming a value, and retiring one that older rows still reference.
- TODO: Compare storage and index cost for an integer, a short string, and a foreign key. See [Status values a person can read](/building-a-saas/07-data-layer/overview#status-values-a-person-can-read).

## Fluent API and annotations

Which one this site prefers, and why.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Getting started](/csharp/entity-framework/getting-started)
- [Database design](/databases/relational/database-design)

---

**Next:** [Querying](/csharp/entity-framework/querying)
