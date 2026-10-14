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

## How modules collaborate

<!-- TODO: An in-process call through the public contract, or an integration event -->

## Tests for the boundaries

<!-- TODO: Fail the build when one module references another's internals -->

## Moving a module out later

<!-- TODO: The contract and the data that would have to travel with it -->

## Practical Examples

- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview) - The monolith, split into modules

## Related Topics

- See [Architecture tests](/patterns/architecture-styles/architecture-tests)
- See [SDLC: Architecture](/sdlc/architecture)
- See [Architecture styles](/patterns/architecture-styles/overview)

---

**Next:** [Architecture Tests](/patterns/architecture-styles/architecture-tests)
