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

### Data ownership

### In-process versus async integration

### Extraction path

## Vertical slice

### Organizing by feature

### Anatomy of a slice

### Sharing code without coupling

### With or without MediatR

## Clients and the server

Business rules stay on the server. Clients render and call.

## Trade-offs

How to write down a decision and the option you did not take.

## Decisions you can undo and ones you can't

- TODO: A choice you can reverse, such as a cache, a queue, or a deploy layout, can be made quickly.
- TODO: A choice that is costly to undo, such as the shape of stored data, a public contract, or a consistency promise, gets a slower decision.
- TODO: Leave a seam so the next change replaces one part. The prototype and the later system do not have to share every choice.
- TODO: Write the condition that would make you take the next step before you need it.

## Reviewing a design for production

- TODO: Walk a design for what production will demand of it. See [A production-readiness review](/building-a-saas/02-architecture-decisions/overview#a-production-readiness-review).

## Diagrams that match the code

- TODO: A diagram drawn by hand goes stale when the projects move and the picture does not.

### Having an agent draw it

- TODO: Build the diagram from project references and from the contracts each module exposes.
- TODO: Store it as Mermaid in the repository, where a pull request can show the change, or draw it on a board through that board's MCP server.
- TODO: The agent proposes the picture. Compare it with the architecture tests before you accept it. See [Architecture tests](/patterns/architecture-styles/architecture-tests).
- TODO: Draw it again when a pull request changes which modules depend on which.
- TODO: Writing the board is a permissions choice. Decide who may publish, and who may only propose. See [Regenerating the diagram](/building-a-saas/02-architecture-decisions/overview#regenerating-the-diagram).

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Building a SaaS: Architecture](/building-a-saas/02-architecture-decisions/overview)
- [Modular monolith](/patterns/architecture-styles/modular-monolith)
- [Platform](/csharp/platform/overview)

---

**Next:** [Requirements and Stories](/sdlc/requirements-and-stories)
