---
title: Playwright for .NET
order: 65
---

# Playwright for .NET

A few browser tests that drive the real UI. They live in the same test project as the rest of the suite.

## Browsers on the build agent

- TODO: Install the browsers the suite needs in CI, and reuse them across runs so the job does not download them every time.
- TODO: Fail the job when the browser build and the library build disagree.

## Finding elements

- TODO: Locate an element by its role or its label, and let the library wait until that element is ready.
- TODO: A fixed sleep hides a race. Wait on the condition the locator already knows how to wait for.

## Where the app runs

- TODO: Point the browser at the app booted in-process, or at an environment that is already deployed.
- TODO: The in-process host is [ASP.NET Core tests](/csharp/testing/webapplicationfactory). A deployed environment is a separate address and a separate set of secrets.

## One sign-in

- TODO: Sign in once, save that browser state, and reuse it for the tests that need an authenticated session.
- TODO: A test for a different user gets its own state. Do not share one session across tenants.

## When a test fails

- TODO: Keep a trace and a screenshot for a failure, and discard them when the test passes.
- TODO: The trace is how you see which step waited until it gave up.

## Pictures for the docs

- TODO: The same run can capture a screenshot of a screen the docs describe.
- TODO: Treat the picture as generated. Make it again when the screen changes.

## How few is enough

- TODO: Keep an end-to-end test for a path a unit test cannot see, such as sign-in through to one saved change.
- TODO: Leave everything else in the unit and integration layers. Where this product draws that line is [End-to-end tests](/building-a-saas/10-testing-strategy/overview#end-to-end-tests).

## Related Topics

- See [bUnit](/csharp/testing/bunit)
- See [ASP.NET Core tests](/csharp/testing/webapplicationfactory)
- See [Building a SaaS: Testing Strategy](/building-a-saas/10-testing-strategy/overview)

---

**Next:** [Integration Testing](/csharp/testing/integration-testing)
