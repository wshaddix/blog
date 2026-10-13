---
title: Seeding
order: 30
---

# Seeding

Reference data the app assumes is present.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## HasData

Seed rows in a migration, and the limits of that mechanism.

## Startup seeding

A development-only seed that runs after migrate.

## Ids

A stable key so the next migration does not try to insert the row again.

## Tenants

Seed data that is global, and seed data that must not leak across tenants.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Migrations](/csharp/entity-framework/migrations)

---

**Next:** [Raw SQL](/csharp/entity-framework/raw-sql)
