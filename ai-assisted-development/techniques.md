---
title: Techniques
order: 70
---

# Techniques

Ways of working that make an assistant useful on a real change.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Spec first

Write the outcome and the constraints before asking for code.

### A plan that outlives the session

- TODO: The plan is a file in the repository, with the phases and a checkbox for each one, written before the code changes.
- TODO: A later session reads that file and continues. The plan is not only in the chat.
- TODO: Settle the plan before the agent edits a wide set of files.

## Small diffs

One behavior per request. A giant generation is hard to review and hard to revert.

## Tests as the contract

Ask for a failing test first, or write it yourself and let the assistant make it pass.

## Point at the code

Name the file, the type, and the convention. Do not make the model guess the architecture.

## Iterate on the failure

Paste the compiler error or the test output. Do not restate the whole task.

## Investigating a live failure

- TODO: Scope the brief to one failure: the tenant, the route, and the time window.
- TODO: Pass the trace id so the investigation starts from that trace.
- TODO: Write what the trace and the logs show, and keep the suspected cause beside that evidence until the evidence supports it.

## Stop conditions

A definition of done, and a point where you take the keyboard back.

## Checkpoints

- TODO: A checkpoint is a snapshot of the agent session, so you can return the conversation and its edits to an earlier point in that session.
- TODO: A git commit is the history of the repository. Restore a checkpoint to undo a wrong turn in the session. Commit when the change is one you mean to keep.

## Parallel work in worktrees

- TODO: Give each feature its own worktree, so two agents can change files at the same time without sharing a working directory.
- TODO: A question that does not change files can run in a separate agent. Only the answer comes back to the session that edits.
- TODO: Merge a worktree when its tests pass. The other feature stays in its own worktree.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [Prompting](/ai-assisted-development/prompting)
- [Verification](/ai-assisted-development/verification)
- [Testing strategy](/sdlc/testing-strategy)
- [Observability](/csharp/aspnet-core/observability/overview)

---

**Next:** [Prompting](/ai-assisted-development/prompting)
