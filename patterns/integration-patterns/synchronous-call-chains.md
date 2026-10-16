# Synchronous Call Chains

A request that waits on another module, which waits on another, stacks latency and failure.

## One request, many waits

- TODO: Draw the modules a single call touches before it returns.
- TODO: Each extra hop adds its own latency, and the caller cannot finish until the last one does.

## Timeouts along the chain

- TODO: The outer deadline has to be longer than the inner ones, or the caller gives up while work is still running.
- TODO: A timeout does not tell you whether the downstream call committed.

## Where a message fits better

- TODO: A step the user does not need in the response can leave the request and travel as a message.
- TODO: The modules that stay in the request are the ones that share the user's answer.

## Practical Examples

- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview) - Calls between modules
- See [Building a SaaS: Monitoring and Operations](/building-a-saas/12-monitoring-operations/overview) - A trace of the chain

## Related Topics

- See [Modular monolith](/patterns/architecture-styles/modular-monolith)
- See [Sagas](/patterns/integration-patterns/sagas)
- See [Observability](/csharp/aspnet-core/observability/overview)

---

**Next:** [Event Sourcing and Change Data Capture](/patterns/architecture-styles/event-sourcing-and-cdc)
