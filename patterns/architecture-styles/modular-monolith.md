# Modular Monolith

One deployable, divided into modules that own their data and their features.

## A module

## Slices inside the module

### What a slice contains

## Public contracts

## Data ownership

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

## Tests for the boundaries

## Moving a module out later

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
