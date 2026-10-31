# Kubernetes

A cluster that places containers, restarts them, and gives them a stable name.

## What the cluster takes on

Placement, restarts, and a name for the service come with the cluster. The application still owns its data and its correctness.

- TODO: List what the cluster handles: where a process runs, restarting it, a rolling update, and a stable service name.
- TODO: List what it leaves to the app: transactions, schema changes, and a bug that still answers a health check.

## Health probes

A probe is an HTTP call to a health check the process already exposes.

- TODO: Map a liveness probe, a readiness probe, and a startup probe onto the checks in [Health checks](/csharp/aspnet-core/observability/health-checks).
- TODO: A failed readiness probe takes the pod out of service. A failed liveness probe restarts it.

## A pod that keeps restarting

The useful record is why the process exited, including the previous container's logs.

- TODO: Read that previous log and the exit code before changing a probe or a limit.
- TODO: Separate a crash from a probe that kills a process still starting.

## Requests and limits for a .NET process

The scheduler places a pod from its request. The node kills the process that passes its memory limit.

- TODO: Set a request the cluster can place, and a limit the process is allowed to reach.
- TODO: Leave room for the garbage collector. A memory limit tight against the working set gets the process killed under load.

## What the application has to change

A process that can be stopped and started on another machine cannot keep its only copy of state in memory.

- TODO: Read configuration from the environment, and finish requests that are already in flight when shutdown starts.
- TODO: Keep session and cache data outside the process, so a restart continues from shared state.

## When one host is no longer enough

Move to a cluster when a single machine cannot meet the availability or the capacity you already measure.

- TODO: Name the signs: no room for another instance, a restart that takes the product offline, and a deploy that cannot roll while traffic is live.
- TODO: Until those signs are real, this product stays on one host. See [Why not Kubernetes yet](/building-a-saas/11-deployment/overview#why-not-kubernetes-yet).

## Related Topics

- See [Docker Fundamentals](/devops/containerization/docker-fundamentals)
- See [Container Best Practices](/devops/containerization/best-practices)
- See [Health checks](/csharp/aspnet-core/observability/health-checks)

---

**Next:** [Azure Overview](/devops/azure/overview)
