---
title: Migrations
order: 60
---

# Migrations

Evolving your database schema over time.

## What are Migrations?

<!-- TODO: Version control for your database -->

## Creating Migrations

<!-- TODO: Add-Migration, dotnet ef migrations add -->

## Applying Migrations

<!-- TODO: Update-Database, dotnet ef database update -->

## Migration Files

<!-- TODO: Up, Down, ModelSnapshot -->

## Best Practices

<!-- TODO: Small migrations, testing, CI/CD -->

## Handling Data

<!-- TODO: Data migrations, seed data -->

## Changing a column without downtime

During a rolling deploy the previous version and the new one share the database, so a column change has to be valid for both.

- TODO: Explain why a rename breaks the old version, which still reads and writes the previous name.
- TODO: Add the new shape beside the old one, and leave the old column in place.
- TODO: Write both shapes on every change while both versions are still running.
- TODO: Backfill rows that already exist before any reader depends on the new shape.
- TODO: Switch reads to the new shape only after that backfill and the dual write are in place.
- TODO: Drop the old shape in a later release, once no running version still uses it.
- TODO: Split those steps into separate EF migrations so a release applies only the step it is ready for. See [Expand, then contract](/building-a-saas/11-deployment/overview#expand-then-contract).

---

**Next:** [Performance](/csharp/entity-framework/performance)
