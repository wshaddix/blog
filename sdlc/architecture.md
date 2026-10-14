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

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Building a SaaS: Architecture](/building-a-saas/02-architecture-decisions/overview)
- [Modular monolith](/patterns/architecture-styles/modular-monolith)
- [Platform](/csharp/platform/overview)

---

**Next:** [Requirements and Stories](/sdlc/requirements-and-stories)
