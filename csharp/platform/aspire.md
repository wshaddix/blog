# .NET Aspire

Orchestrate the local dependencies of a multi-project app.

## Aspire AppHost for local dev

## In the SaaS app

## Beyond the AppHost

- TODO: The dashboard can be published with native AOT when that tool needs a short startup and a small output.
- TODO: A test UI resource in the app model gives a page that drives the system under test from the same dashboard as the other resources.

### Services in other languages

- TODO: A service that is not a .NET project can still be a resource in the AppHost. Point it at the directory and the command that starts the process.
- TODO: The dashboard lists that process with the .NET projects. A .NET project receives its address by referencing the resource.
- TODO: The other resources wait until its endpoint is ready, the same way they wait for a .NET project.

### A local multi-node cluster

- TODO: Start several copies of one service and let them form a cluster on the machine. Each copy is its own process with its own endpoint.
- TODO: They find each other through a discovery resource the AppHost starts first, such as Redis. The AppHost injects that connection into each copy.
- TODO: The dashboard shows logs, health, and membership for every node, so a local cluster can be debugged without a hand-written seed list.

## Practical Examples

- See [Building a SaaS: Project Setup](/building-a-saas/01-project-setup/overview)

## Related Topics

- See [Generic Host](/csharp/platform/generic-host)
- See [Projects and Solutions](/csharp/language-basics/projects-and-solutions)
- See [Publishing](/csharp/platform/publishing)

---

**Next:** [Dependency Injection](/csharp/platform/dependency-injection)
