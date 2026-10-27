# Chapter 2: Architecture Decisions

Good architecture enables teams to move fast while maintaining quality. Here we make key decisions for our SaaS platform.

## What We'll Cover

- Layered architecture choices
- When to use which patterns
- Monolith vs microservices (spoiler: we start monolith)
- When a module leaves the monolith
- Choosing the stack
- CQRS and when it makes sense
- Dependency injection setup

## Our Architecture

## Why Monolith First?

## Choosing the stack

- TODO: Pick .NET when the team will live in this language, the host runs it, and the libraries you need already exist for it.
- TODO: Record the workload that would move the choice to another runtime, and why this product stays on .NET.

## Modular monolith

## When a module leaves

- TODO: The first module to leave is the one whose contract and data can move without dragging the rest of the process along.
- TODO: Keep a module in-process while other modules still share its transaction or read its tables.

### Strangling the module out

- TODO: Send one slice of the module's calls to the new process and leave the rest on the path that already runs.
- TODO: Widen the slice after the new path is the one callers use, and remove the old path when it has no traffic.

## Calls between modules

- TODO: A module calls another through its public contract, in process, or by publishing an event.
- TODO: A chain of synchronous calls stacks latency. Trace that chain before adding another hop.

## Consistency per operation

- TODO: A payment or a seat change needs one current answer. A feed or a count can lag.
- TODO: Choose that per operation. One consistency mode for the whole product is the wrong default.

## Patterns We'll Use

The public API stays JSON over HTTP. gRPC is a decision only when an internal client needs an HTTP/2 contract.

## Dependency Injection

## Decision records

- TODO: A proposal from the team states the intent and the options. The record states the choice and what was turned down.
- TODO: A check in the build fails when new code crosses that choice, so the record is not the only thing holding it.

### Triggers for the next step

- TODO: The record names the measurement that would change the decision, such as a latency figure or a number of tenants.
- TODO: Write that trigger while the choice is still easy to revisit.
- TODO: When the trigger is true, the record already says which part moves and which part stays.

## A production-readiness review

- TODO: Review a design against what production will require before the build starts. See [Reviewing a design for production](/sdlc/architecture#reviewing-a-design-for-production).

## Key Principles

1. **Simplicity first** - Don't add patterns until you need them
2. **Testability** - Architecture should make testing easy
3. **Boundaries** - Clear separation between concerns
4. **Flexibility** - Easy to change decisions later

## Related Topics

- See [C# and .NET](/csharp/overview)
- See [Modular monolith](/patterns/architecture-styles/modular-monolith)
- See [Distributed building blocks](/patterns/architecture-styles/distributed-building-blocks)
- See [Synchronous call chains](/patterns/integration-patterns/synchronous-call-chains)
- See [Consistency](/fundamentals/distributed-systems/consistency)
- See [Decision making](/career-development/team-operations/decision-making)
- See [gRPC](/csharp/aspnet-core/web-apis/grpc)
- See [SDLC: Architecture](/sdlc/architecture)

---

**Next:** [Chapter 3: Domain Modeling](/building-a-saas/03-domain-modeling/overview)
