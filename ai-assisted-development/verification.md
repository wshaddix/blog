# Verification

Generated code is a draft. The same checks apply as if a new teammate wrote it.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Read the diff

Every file. Look for extra changes you did not ask for.

## Build and test

The project's tests, on TUnit. A green run is the minimum.

### A reproduction you checked yourself

A test written in the same pass as the fix can pass because it shares the fix's assumption.

- TODO: Write the reproduction before anyone changes the code, and run it so the failure is visible.
- TODO: Change the code only after that failure is the one you meant, then run the same test and watch it pass.
- TODO: Leave the test in the suite so the bug cannot return quietly. See [Bug fixes start with a failing test](/building-a-saas/10-testing-strategy/overview#bug-fixes-start-with-a-failing-test).

## Behavior

Exercise the path a user hits when the change is visible.

## Ask for a critique

A second pass that lists risks is useful after the code exists, not instead of reading it.

## Evals for prompts

When a prompt is reused, keep a few cases and re-run them after you edit the prompt.

## Trying to break the feature

- TODO: After the happy path works, ask the agent for inputs that should fail: an empty body, a second submit, the wrong tenant, a call that gets cancelled.
- TODO: Reproduce each finding yourself. A suggestion is not a failing test until you can run it again.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [Code review](/sdlc/code-review)
- [TUnit project setup](/csharp/testing/project-setup)
- [Building a SaaS: Testing Strategy](/building-a-saas/10-testing-strategy/overview)

---

**Next:** [Using MCP](/ai-assisted-development/using-mcp)
