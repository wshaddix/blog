# GitHub Actions

Automation built into GitHub for CI/CD workflows.

## Workflow Basics

### Cancelling an older deploy

- TODO: A concurrency group cancels the older in-progress deploy when a newer run for that group starts.

## Common Triggers

## Building .NET Applications

## Deploying to Azure

## Secrets and Variables

## Reusable Workflows

## Pinning actions

- TODO: A tag can move. A workflow that names a tag runs whatever commit that tag points at on the day the job starts.
- TODO: Pin the action to a commit. When you move the pin, review the diff between the two commits.
- TODO: An action may call further actions. Pinning the outer action does not pin the ones it calls.
- TODO: How the release workflow for this product is pinned is [Pinning the workflow](/building-a-saas/11-deployment/overview#pinning-the-workflow).

## A scheduled link check

- TODO: On a schedule, request the pages of the site and fail the job when an internal link does not resolve.
- TODO: A weekly run catches a link that broke after the pull request that added it had already passed.

---

**Next:** [Azure DevOps](/devops/ci-cd/azure-devops)
