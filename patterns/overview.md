# Design Patterns

Patterns are proven solutions to common problems. Understanding them helps you write better code and communicate with other engineers.

## Taught on this path

These are lessons. The long lists further down this section are catalogs of names.

- [Repository](/patterns/application-patterns/repository) - A collection-shaped front for one aggregate
- [CQRS](/patterns/application-patterns/cqrs) - A write model and a read model, when they have diverged
- [Decorator](/patterns/coding-patterns/decorator) - The shape behind middleware and HTTP handlers
- [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer) - One transaction for the state change and the message
- [Sagas](/patterns/integration-patterns/sagas) - Multi-step workflows across services
- [Choreography and orchestration](/patterns/integration-patterns/choreography-vs-orchestration) - Who decides the next step
- [Modular monolith](/patterns/architecture-styles/modular-monolith) - One deployable, modules that own their data, slices inside each module
- [Architecture tests](/patterns/architecture-styles/architecture-tests) - Fail the build when a boundary is crossed
- [Event sourcing and change data capture](/patterns/architecture-styles/event-sourcing-and-cdc) - A stream of facts

## What's Covered

### Coding Patterns (GoF)

The classic "Gang of Four" design patterns:

- [Creational Patterns](/patterns/coding-patterns/creational-patterns/singleton-pattern) - Object creation mechanisms
- [Structural Patterns](/patterns/coding-patterns/structural-patterns/overview) - Object composition
- [Behavioral Patterns](/patterns/coding-patterns/behavioral-patterns/overview) - Object communication

### Application Patterns

Higher-level patterns for structuring applications:

- [Repository Pattern](/patterns/application-patterns/overview) - Data access abstraction
- [CQRS](/patterns/application-patterns/overview) - Command/Query separation
- [Unit of Work](/patterns/application-patterns/overview) - Transaction management

### Integration Patterns

Patterns for connecting systems:

- [API Patterns](/patterns/integration-patterns/overview) - REST, versioning, pagination
- [Messaging Patterns](/patterns/integration-patterns/overview) - Async communication
- [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer) - State and the message commit together
- [Sagas](/patterns/integration-patterns/sagas) - Multi-step workflows across services
- [Choreography and orchestration](/patterns/integration-patterns/choreography-vs-orchestration) - Who decides the next step

### Architecture Styles

- [Overview](/patterns/architecture-styles/overview) - Slicing a codebase
- [Modular monolith](/patterns/architecture-styles/modular-monolith) - Modules, slices, and data ownership
- [Architecture tests](/patterns/architecture-styles/architecture-tests) - Enforcing boundaries
- [Event sourcing and change data capture](/patterns/architecture-styles/event-sourcing-and-cdc) - A stream of facts

### Refactoring Patterns

Techniques for improving existing code:

- [Code Smells](/patterns/refactoring-patterns/overview) - Recognizing problems
- [Refactoring Techniques](/patterns/refactoring-patterns/overview) - Safe transformations

## How to Use This Section

1. **Learn the vocabulary** - Pattern names are a shared language
2. **Understand the problem first** - Patterns solve specific problems
3. **Don't force patterns** - Simpler is often better
4. **See them in context** - [Building a SaaS](/building-a-saas/overview) applies many patterns

## Anti-Patterns

Equally important is knowing what *not* to do:

- Over-engineering (too many patterns)
- Wrong pattern for the problem
- Patterns without understanding the "why"

---

*Start with [Coding Patterns](/patterns/coding-patterns/overview) for the classics, or explore [Application Patterns](/patterns/application-patterns/overview) for practical architecture.*
