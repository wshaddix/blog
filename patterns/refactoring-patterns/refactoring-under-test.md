---
title: Refactoring Under Test
order: 0
---

# Refactoring Under Test

Change the shape of code that already runs by recording what it does before you move it.

## Characterization tests

A characterization test freezes today's output, including behavior nobody has called correct yet.

- TODO: Record the current output with a characterization test or a snapshot before any structure changes.
- TODO: Treat that recording as the net for the edits that follow, not as a spec you meant to design.

## A wide spread of inputs

The pinned behavior is only as wide as the inputs you recorded.

- TODO: Pick inputs that reach the branches, the edges, and the combinations the rules actually see.
- TODO: Add a case when the next edit would move a branch no test touches.

## Small steps

Each edit stays small enough that a green run still names the move that changed the output.

- TODO: Keep the suite green between steps, and undo the last step when it goes red.
- TODO: Make each commit a step you can stop on, with the suite green at that point.

## One rule in one place

Nested conditions hide a single rule inside the rest, so one change means rereading all of them.

- TODO: Move one rule into its own type or method, and leave the others until the suite is green again.
- TODO: Repeat until a rule can change without reading the ones beside it.

## Tests that pinned a bug

A characterization test can demand a bug you sat down to remove.

- TODO: Delete or rewrite a test that records a bug this refactor is supposed to fix.
- TODO: Do that on purpose, after the structure is safe, so the suite stops requiring the old bug.

## A walk-through

A small rules class is enough to show the sequence in C#.

- TODO: Walk through one small rules class with TUnit: pin the output, spread the inputs, extract one rule at a time, and drop a test that protected a bug.
- TODO: The same sequence, applied to domain logic in the product, is [Pinning behavior before a refactor](/building-a-saas/10-testing-strategy/overview#pinning-behavior-before-a-refactor).

## Related Topics

- See [Unit testing](/csharp/testing/unit-testing)
- See [Building a SaaS: Testing Strategy](/building-a-saas/10-testing-strategy/overview)

---

**Next:** [Integration Patterns](/patterns/integration-patterns/overview)
