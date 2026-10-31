# CI/CD Concepts

Continuous Integration and Continuous Delivery automate the path from code to production.

## Continuous Integration (CI)

### Running the checks on your own machine

The suite can run on a developer machine before the commit is pushed, which changes what the hosted runner is for.

- TODO: Spell out what a hosted runner costs in wait time and in the bill when every pull request runs the full suite.
- TODO: Keep a single script that both the local hook and the pipeline call, so the two paths cannot drift.
- TODO: Skip the hosted run for a commit whose local run of that script already passed.
- TODO: Send that pass back to the pull request so the review shows it.
- TODO: Say when a team is too large for a local pass to stand in for the hosted run.
- TODO: Keep a nightly hosted run as the backstop for commits the local gate did not cover. See [One script for local and hosted checks](/building-a-saas/01-project-setup/overview#one-script-for-local-and-hosted-checks).

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
