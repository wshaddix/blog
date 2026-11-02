# Chapter 10: Testing Strategy

Tests give you confidence to ship. We'll build a comprehensive testing strategy.

## What We'll Cover

- Test pyramid for our SaaS
- Unit testing domain logic
- Integration testing APIs
- Testing multi-tenant scenarios
- Test data management
- CI integration

## Our Test Pyramid

```
        /\
       /  \    E2E (few, slow, high confidence)
      /----\
     /      \  Integration (more, medium speed)
    /--------\
   /          \ Unit (many, fast, focused)
  /------------\
```

## Unit Tests

### Bug fixes start with a failing test

A bug fix arrives with a test that already failed on the code it replaces.

- TODO: Take the reproduction you ran, turn it into a test, and see that test fail before editing the production code.
- TODO: A test added in the same edit as the fix is not evidence until that failure has been seen. See [A reproduction you checked yourself](/ai-assisted-development/verification#a-reproduction-you-checked-yourself).

### Pinning behavior before a refactor

A refactor of domain logic starts from tests that record what the code does today.

- TODO: Capture the current output, then change the structure in small steps that leave those tests green.
- TODO: Remove a test that locked in a bug this change is meant to fix. See [Refactoring under test](/patterns/refactoring-patterns/refactoring-under-test).

### A nested pricing rule

A price that depends on several checks often hides the real rule under the last `else`.

- TODO: Find the rule at the deepest indent, where every `else` returns a default price.
- TODO: Return early for the exits first: a missing input, an inactive plan, and a quantity that does not meet the threshold.
- TODO: Keep every branch. The edit removes the nesting, so the depth drops and the branch count stays.
- TODO: Pin each exit with a test before the code that handles that exit moves.
- TODO: When the early returns are still a pile of conditions, name the decision as a predicate or a specification.
- TODO: Trace every path from the first line to the last, and check that a reader can follow it from top to bottom.
- TODO: The move, written as a refactoring step, is [Flattening nested conditionals](/patterns/refactoring-patterns/refactoring-under-test#flattening-nested-conditionals).

### Names from the domain

A unit test in this product is named for the business rule it guards.

- TODO: Put the rule in the name. A name that describes the assertion machinery hides which rule failed.
- TODO: `Fails_the_greater_than_check` is the weak form of a seat limit. `Refuses_a_member_past_the_seat_limit` is the rule.
- TODO: When the test fails, the name alone should identify the rule.
- TODO: Keep one class per behavior and one case per boundary, grouped by the rule.
- TODO: Treat the names as the notes the next person or the next agent uses to edit the code.
- TODO: A review check: a product person can read the test list and recognize the rules.
- TODO: How to name the method is [Names that state the rule](/csharp/testing/unit-testing#names-that-state-the-rule).

## Integration Tests

## Testing Multi-Tenancy

### Two tenants in every fixture

Isolation shows up only when the fixture holds two tenants that could be mistaken for each other.

- TODO: Call data access with a tenant argument. A helper that omits it is a failing test, not a convenience.
- TODO: Include the paths a global filter skips: `IgnoreQueryFilters`, raw SQL, Dapper, a reporting view, and a background job.
- TODO: Cover cache keys, a search or vector index, a blob path, an export, and a log field in the same fixture.
- TODO: Assert the tenant predicate is part of the index query, ahead of ranking.
- TODO: Seed two tenants with similar rows. Sign in as tenant A, request tenant B's ids on every endpoint, and expect 404.
- TODO: When an agent wrote the query, fail the review if the tenant check is missing. See [Paths that skip the filter](/building-a-saas/05-multi-tenancy/overview#paths-that-skip-the-filter) and [Retrieval across tenants](/ai-assisted-development/risks-and-limits#retrieval-across-tenants).

## Architecture tests

## Time-dependent tests

## Test data management

- TODO: Seed tenants of different sizes. One large tenant is the case that exposes a bad query.
- TODO: Make the seed repeatable so a failure is the query, not a random row count.

## Trying to break the feature

- TODO: Point an agent at one feature and ask for cases the happy path never runs: the wrong tenant, a double submit, a missing field.
- TODO: Keep the cases that reproduce. A suggestion you cannot run again is not part of the suite.

## Evals against a second model

- TODO: Run the same evals against the replacement before switching, as in [Changing the model without changing the feature](/csharp/mcp/clients-and-agents#changing-the-model-without-changing-the-feature), and keep the checks in [Verification](/ai-assisted-development/verification).

### Trying smaller models

- TODO: Try a smaller model against those same evals and keep it when it passes. See [The smallest model that passes](/csharp/mcp/clients-and-agents#the-smallest-model-that-passes).

## Related Topics

- See [C#: Testing](/csharp/testing/unit-testing) - TUnit, TUnit.Mocks, and API tests
- See [Reqnroll](/csharp/testing/reqnroll/overview) - Behavior scenarios on the TUnit runner
- See [Architecture tests](/patterns/architecture-styles/architecture-tests)
- See [Time-dependent code](/csharp/testing/time-dependent-code)
- See [Entity Framework performance](/csharp/entity-framework/performance)
- See [Verification](/ai-assisted-development/verification)

---

**Next:** [Chapter 11: Deployment](/building-a-saas/11-deployment/overview)
