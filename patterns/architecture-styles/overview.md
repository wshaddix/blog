---
title: Overview
order: 30
---

# Architecture Styles

How a codebase is sliced, and how those slices are kept from leaking.

## In this section

- [Modular monolith](/patterns/architecture-styles/modular-monolith) - One deployable, a schema and a `DbContext` per module, and how to find the boundaries.
- [Architecture tests](/patterns/architecture-styles/architecture-tests) - Rules that fail the build when a boundary is crossed.
- [Event sourcing and change data capture](/patterns/architecture-styles/event-sourcing-and-cdc) - A log of facts, and a stream read from the database log.
- [Distributed building blocks](/patterns/architecture-styles/distributed-building-blocks) - A gateway, discovery, a sidecar, a strangler, and the reason each would come back out.

## Practical Examples

- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview) - The monolith-first and vertical-slice decision

## Related Topics

- See [SDLC: Architecture](/sdlc/architecture) - Layers, boundaries, and a modular monolith

---

**Next:** [Modular Monolith](/patterns/architecture-styles/modular-monolith)
