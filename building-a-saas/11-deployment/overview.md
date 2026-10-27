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

## Azure Deployment

<!-- TODO: App Service, slots, configuration -->

## Database Migrations

<!-- TODO: Safe migration strategies -->

## Deployment Strategies

| Strategy | Description | Risk |
|----------|-------------|------|
| Rolling | Gradual replacement | Low |
| Blue-Green | Instant switch | Medium |
| Canary | Gradual traffic shift | Low |

## Related Topics

- See [Publishing](/csharp/platform/publishing)
- See [DevOps: CI/CD](/devops/ci-cd/concepts)
- See [DevOps: Containerization](/devops/containerization/docker-fundamentals)
- See [DevOps: Azure](/devops/azure/overview)

---

**Next:** [Chapter 12: Monitoring & Operations](/building-a-saas/12-monitoring-operations/overview)
