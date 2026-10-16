---
title: Overview
order: 1
---

# Chapter 2: Architecture Decisions

Good architecture enables teams to move fast while maintaining quality. Here we make key decisions for our SaaS platform.

## What We'll Cover

- Layered architecture choices
- When to use which patterns
- Monolith vs microservices (spoiler: we start monolith)
- CQRS and when it makes sense
- Dependency injection setup

## Our Architecture

<!-- TODO: Clean Architecture / Vertical Slices hybrid -->

## Why Monolith First?

<!-- TODO: Premature optimization, splitting later -->

## Modular monolith

<!-- TODO: Modules that own their schema, with vertical slices inside each module -->

## Calls between modules

- TODO: A module calls another through its public contract, in process, or by publishing an event.
- TODO: A chain of synchronous calls stacks latency. Trace that chain before adding another hop.

## Consistency per operation

- TODO: A payment or a seat change needs one current answer. A feed or a count can lag.
- TODO: Choose that per operation. One consistency mode for the whole product is the wrong default.

## Patterns We'll Use

<!-- TODO: Repository, CQRS-lite, MediatR decision -->

The public API stays JSON over HTTP. gRPC is a decision only when an internal client needs an HTTP/2 contract.

## Dependency Injection

<!-- TODO: Service registration, lifetimes -->

## Key Principles

1. **Simplicity first** - Don't add patterns until you need them
2. **Testability** - Architecture should make testing easy
3. **Boundaries** - Clear separation between concerns
4. **Flexibility** - Easy to change decisions later

## Related Topics

- See [Modular monolith](/patterns/architecture-styles/modular-monolith)
- See [Synchronous call chains](/patterns/integration-patterns/synchronous-call-chains)
- See [Consistency](/fundamentals/distributed-systems/consistency)
- See [gRPC](/csharp/aspnet-core/web-apis/grpc)
- See [SDLC: Architecture](/sdlc/architecture)

---

**Next:** [Chapter 3: Domain Modeling](/building-a-saas/03-domain-modeling/overview)
