---
title: Architecture
order: 90
---

# Architecture

Where the code of a console app, an API, a web UI, a Windows app, and a mobile app each sits.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Layers

What belongs in the domain, the application, the infrastructure, and the host.

## Boundaries

A project reference is a dependency. Draw the ones you mean to keep.

## A modular monolith

One deployable with internal boundaries, and when that is the right shape.

### Module boundaries and public contracts

<!-- TODO -->

### Data ownership

<!-- TODO: Schema per module -->

### In-process versus async integration

<!-- TODO -->

### Extraction path

<!-- TODO: What would have to move if a module left the process -->

## Vertical slice

<!-- TODO: Organize by feature -->

### Organizing by feature

<!-- TODO -->

### Anatomy of a slice

<!-- TODO: Endpoint, handler, validator, test -->

### Sharing code without coupling

<!-- TODO -->

### With or without MediatR

<!-- TODO -->

## Clients and the server

Business rules stay on the server. Clients render and call.

## Trade-offs

How to write down a decision and the option you did not take.

## Decisions you can undo and ones you can't

- TODO: A choice you can reverse, such as a cache, a queue, or a deploy layout, can be made quickly.
- TODO: A choice that is costly to undo, such as the shape of stored data, a public contract, or a consistency promise, gets a slower decision.
- TODO: Leave a seam so the next change replaces one part. The prototype and the later system do not have to share every choice.
- TODO: Write the condition that would make you take the next step before you need it.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Building a SaaS: Architecture](/building-a-saas/02-architecture-decisions/overview)
- [Modular monolith](/patterns/architecture-styles/modular-monolith)
- [Platform](/csharp/platform/overview)

---

**Next:** [Requirements and Stories](/sdlc/requirements-and-stories)
