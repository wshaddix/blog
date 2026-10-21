---
title: Distributed Building Blocks
order: 5
---

# Distributed Building Blocks

Parts a split system often adds, and the condition that would make each one leave again.

## API gateway

- TODO: A gateway accepts the client connection and routes it to a service.
- TODO: Drop the gateway when one service is already that front door and the gateway only forwards.

## Service discovery

- TODO: Discovery tells a caller which instance is live when addresses change.
- TODO: Drop discovery when the addresses are fixed and configuration already names them.

## Sidecar

- TODO: A sidecar is a process beside the app that handles one concern, such as a proxy or telemetry.
- TODO: Drop the sidecar when the app already handles that concern and the extra process is only another deploy.

## Strangler fig

- TODO: A strangler sends one slice of calls to the new module and leaves the rest on the old path.
- TODO: Remove the split once every caller uses the new module and the old path has no traffic.

## Anti-corruption layer

- TODO: An anti-corruption layer translates another system's model so this module keeps its own.
- TODO: Remove the layer when both sides are yours and they can share one contract.

## Sharding

- TODO: Sharding splits data so one store does not hold all of it.
- TODO: Stay on one store while that store still answers in the time the product needs.

## Replication

- TODO: Replication copies data so a read can be served from another copy and one loss is survivable.
- TODO: Remove a replica that no read uses and that failover does not need.

## Practical Examples

- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview) - Strangling a module out
- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - Read replicas

## Related Topics

- See [Modular monolith](/patterns/architecture-styles/modular-monolith)
- See [Consistency](/fundamentals/distributed-systems/consistency)
- See [Synchronous call chains](/patterns/integration-patterns/synchronous-call-chains)

---

**Next:** [Chapter 3: Domain Modeling](/building-a-saas/03-domain-modeling/overview)
