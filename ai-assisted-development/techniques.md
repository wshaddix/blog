# Techniques

Ways of working that make an assistant useful on a real change.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Spec first

Write the outcome and the constraints before asking for code.

## Small diffs

One behavior per request. A giant generation is hard to review and hard to revert.

## Tests as the contract

Ask for a failing test first, or write it yourself and let the assistant make it pass.

## Point at the code

Name the file, the type, and the convention. Do not make the model guess the architecture.

## Iterate on the failure

Paste the compiler error or the test output. Do not restate the whole task.

## Stop conditions

A definition of done, and a point where you take the keyboard back.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [Prompting](/ai-assisted-development/prompting)
- [Verification](/ai-assisted-development/verification)
- [Testing strategy](/sdlc/testing-strategy)

---

**Next:** [Prompting](/ai-assisted-development/prompting)
