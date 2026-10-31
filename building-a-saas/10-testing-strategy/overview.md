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

## Integration Tests

## Testing Multi-Tenancy

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
