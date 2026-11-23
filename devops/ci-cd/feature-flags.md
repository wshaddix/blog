---
title: Feature Flags
order: 4
---

# Feature Flags

Putting a build on the host and letting callers use a feature are two decisions.

## A deploy and a release

- TODO: A deploy places the build. A release lets a caller exercise the new behavior.
- TODO: The flag is how those two move on different days.

## Who the flag applies to

- TODO: Turn a feature on for a percentage of calls, for a window of time, or for one tenant.
- TODO: Use the filters in Microsoft.FeatureManagement for those three, and add a filter of your own only for a rule they do not cover.

## Where the state lives

- TODO: Store the flag where it can change without shipping another build.
- TODO: A process may cache the value. Bound how long a stale copy is allowed to live.

## Turning a feature off

- TODO: A flag can disable a feature that is hurting production without rolling the build back.
- TODO: The path that stays enabled has to keep working while the flagged path is off.

## Taking a flag out

- TODO: Give every flag a date it must be gone. A test fails when the flag is still in the code after that date.
- TODO: Delete the flag and the branch it guarded in the same change.

## Beside rolling and blue-green

- TODO: A rolling or blue-green deploy chooses which build receives traffic. A flag chooses which behavior that build runs.
- TODO: How this product releases behind a flag is [Releasing behind a flag](/building-a-saas/11-deployment/overview#releasing-behind-a-flag). A flag that follows a plan is [Flags per plan](/building-a-saas/09-billing-integration/overview#flags-per-plan).

## Related Topics

- See [CI/CD concepts](/devops/ci-cd/concepts)
- See [Building a SaaS: Deployment](/building-a-saas/11-deployment/overview)
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview)

---

**Next:** [GitHub Actions](/devops/ci-cd/github-actions)
