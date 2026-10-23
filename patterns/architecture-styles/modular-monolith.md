---
title: Modular Monolith
order: 25
---

# Modular Monolith

One deployable, divided into modules that own their data and their features.

## A module

<!-- TODO: A named part of the process with a public surface and private internals -->

## Slices inside the module

<!-- TODO: Each feature is a vertical slice that stays inside the module that owns it -->

### What a slice contains

<!-- TODO: The endpoint or handler, the validation, and the test -->

## Public contracts

<!-- TODO: The types and methods other modules are allowed to use -->

## Data ownership

<!-- TODO: The module owns its tables. Queries against those tables stay inside the module -->

### Schema per module

- TODO: Give the module its own database schema, and put its tables there.
- TODO: Another module reaches a row by calling the public contract and passing an id.

### DbContext per module

- TODO: Register one `DbContext` for the module. Its model contains that module's entities.
- TODO: A handler takes the context for its own module.

### A login per module

- TODO: Give that context its own database login, granted only the module's schema.
- TODO: A statement that reads or writes another module's tables fails in the database, which holds the boundary when application code does not.
- TODO: Keep that login's connection string with the module. The string another module uses is described in [A connection string per module](/building-a-saas/07-data-layer/overview#a-connection-string-per-module).

## Finding boundaries

- TODO: List the changes that should ship together. The tables and features on that list are a candidate module.
- TODO: Draw the line where a transaction should stop. Work that must commit together stays in one module.
- TODO: Revisit a line that every feature has to cross.

## How modules collaborate

<!-- TODO: An in-process call through the public contract, or an integration event -->

## Tests for the boundaries

<!-- TODO: Fail the build when one module references another's internals -->

## Moving a module out later

<!-- TODO: The contract and the data that would have to travel with it -->

### The first module to extract

- TODO: Extract the module whose public contract and owned data can move together, while the rest of the process keeps running.
- TODO: Leave a module in-process while other modules still read its tables or share its transaction.

## Practical Examples

- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview) - The monolith, split into modules
- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - A schema and a `DbContext` per module

## Related Topics

- See [Architecture tests](/patterns/architecture-styles/architecture-tests)
- See [DbContext](/csharp/entity-framework/dbcontext)
- See [SDLC: Architecture](/sdlc/architecture)
- See [Architecture styles](/patterns/architecture-styles/overview)

---

**Next:** [Architecture Tests](/patterns/architecture-styles/architecture-tests)
