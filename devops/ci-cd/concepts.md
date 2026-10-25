# CI/CD Concepts

Continuous Integration and Continuous Delivery automate the path from code to production.

## Continuous Integration (CI)

## Continuous Delivery (CD)

## Continuous Deployment

## Pipeline Stages

### Headless review

- TODO: A pipeline stage can start an agent with no chat session and give it the diff for that change.
- TODO: The stage publishes a review comment. Merging the change stays a separate decision.

## After the deploy is triggered

- TODO: Send one deploy request, read its status in a separate loop that stops at a timeout, let a newer run supersede an older one, and verify the health endpoint, a key route, and the user flow before calling the release done.

## Best Practices

## Practical Examples

- See [Building a SaaS: Project Setup](/building-a-saas/01-project-setup/overview) - An automated review step
- See [Building a SaaS: Deployment](/building-a-saas/11-deployment/overview) - CI/CD in practice

---

**Next:** [GitHub Actions](/devops/ci-cd/github-actions)
