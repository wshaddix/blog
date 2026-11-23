---
title: Mutation Testing
order: 85
---

# Mutation Testing

A mutation tool edits the code on purpose and checks whether the tests notice.

## What gets changed

- TODO: The tool flips a condition, a constant, or a return, then runs the tests that cover that line.
- TODO: A suite that still passes did not observe the edit.

## A mutant that survived

- TODO: Read a survivor as a behavior no test asserts, not as a number to chase.
- TODO: Add the missing case, or delete code nothing calls.

## Off the pull request

- TODO: A full run is too slow to gate every pull request. Run it on a schedule.
- TODO: The pull request still runs the tests. The mutation run is the nightly check. See [Watching a test fail](/csharp/testing/unit-testing#watching-a-test-fail).

## Related Topics

- See [Unit testing](/csharp/testing/unit-testing)
- See [Building a SaaS: Testing Strategy](/building-a-saas/10-testing-strategy/overview)

---

**Next:** [Unit Testing](/csharp/testing/unit-testing)
