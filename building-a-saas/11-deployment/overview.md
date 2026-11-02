---
title: Overview
order: 1
---

# Chapter 11: Deployment

Getting code to production reliably and repeatedly.

## What We'll Cover

- CI/CD pipeline with GitHub Actions
- Docker containerization
- Azure App Service deployment
- Database migrations in CI/CD
- Environment management
- Deployment strategies

## CI/CD Pipeline

<!-- TODO: Build, test, deploy stages -->

### Checking the release after it lands

- TODO: After the deploy, follow [After the deploy is triggered](/devops/ci-cd/concepts#after-the-deploy-is-triggered) and confirm the running app with [Health Checks](/building-a-saas/12-monitoring-operations/overview#health-checks).

## Containerization

<!-- TODO: Dockerfile, multi-stage builds -->

### Rebuilding for runtime patches

- TODO: A runtime security fix for a self-contained image is a new build. See [Who patches the runtime](/csharp/platform/publishing#who-patches-the-runtime).

### Bundled runtime binaries

An agent feature that embeds a runtime adds that runtime's binary to the image.

- TODO: The app starts the runtime as a local process and talks to it over a local channel. The runtime runs the model and the tool loop, and calls back for tools and permissions.
- TODO: Development points the same feature at a model on the machine. Production points it at a hosted provider, with the key and the endpoint coming from configuration.
- TODO: Read the runtime's default settings and disable anything this product did not turn on.
- TODO: Register only this product's tools. A read-only tool can run without a prompt. A write waits for a person.
- TODO: Stream events to the UI, and put a cap on the round trips in one turn.
- TODO: Pull the runtime binary during the image build. On a build agent that cannot fetch it, use a mirror or a path where the binary is already installed. Count the binary in the image size.
- TODO: Skip the extra runtime when `IChatClient` already covers the feature. See [An embedded agent runtime](/csharp/mcp/clients-and-agents#an-embedded-agent-runtime).

## Azure Deployment

<!-- TODO: App Service, slots, configuration -->

## Database Migrations

<!-- TODO: Safe migration strategies -->

### Expand, then contract

A migration that ships with one release has to leave the previous version able to run.

- TODO: Add the new column beside the old one, backfill, switch readers, and drop the old column only in a later release.
- TODO: Keep each of those steps in its own migration. See [Changing a column without downtime](/csharp/entity-framework/migrations#changing-a-column-without-downtime).

## Deployment Strategies

| Strategy | Description | Risk |
|----------|-------------|------|
| Rolling | Gradual replacement | Low |
| Blue-Green | Instant switch | Medium |
| Canary | Gradual traffic shift | Low |

### A VPS instead of Azure

- TODO: Host the app on a rented machine when Azure App Service is not the target. See [A rented VPS](/devops/self-hosting/overview#a-rented-vps).
- TODO: Keep staging and production on different machines, with secrets split by environment. See [Staging and production on separate machines](/devops/self-hosting/overview#staging-and-production-on-separate-machines).

### Why not Kubernetes yet

One host is enough until restarts, capacity, or a rolling deploy force a cluster.

- TODO: Keep the current host, including a rented machine, until those signs show up. See [Kubernetes](/devops/containerization/kubernetes).
- TODO: A cluster still needs the health checks, the shutdown handling, and a process that can lose its memory and continue.

## Related Topics

- See [Publishing](/csharp/platform/publishing)
- See [DevOps: CI/CD](/devops/ci-cd/concepts)
- See [DevOps: Containerization](/devops/containerization/docker-fundamentals)
- See [DevOps: Azure](/devops/azure/overview)

---

**Next:** [Chapter 12: Monitoring & Operations](/building-a-saas/12-monitoring-operations/overview)
