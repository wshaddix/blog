---
title: Context and Instructions
order: 50
---

# Context and Instructions

The model only knows what is in the window. You decide what that is.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## What to include

The file under edit, the test, and the type it calls. Not the whole repository.

## What to exclude

Secrets, generated output, and a long log with one relevant line.

## Instruction files

`AGENTS.md`, editor rules, and skills. Standing rules for this repository.

### Folder-scoped files

- TODO: Put the rules for one area in a file in that folder, loaded when the agent works there.
- TODO: Keep a rule about one project next to that project. The root file stays the list of rules that apply to every task.

### A short root file

- TODO: The root file names the rules that are true everywhere, and points at the folder files for the rest.
- TODO: Keep it short enough to read in one pass. Split it when it has grown into a manual.

## Skills

- TODO: A prompt you paste on every similar task belongs in a skill: the steps and the constraints, written once and invoked by name.
- TODO: Leave a one-off request as a prompt. Promote it after the same steps have been worth repeating.

## Hooks

- TODO: A hook runs at a fixed moment, such as before a tool call or after a file write.
- TODO: Put a rule in a hook when it has to run every time, not only when the model remembers a file.

### Format after an edit

- TODO: Run the formatter when a file write finishes, so the style rules are applied by the tool.
- TODO: Stop the step when the formatter cannot write the file, and hand that file back to a person.

### Test gate before finishing

- TODO: Run the tests before the agent is allowed to treat the task as done.
- TODO: A failing run keeps the task open. The gate passes when the tests pass.

### Deny edits to tests

- TODO: When the task is to make the current tests pass, block edits to those tests.
- TODO: Changing a test is a separate decision a person makes. The agent's job on that task is to satisfy the tests as they stand.

## Subagents

- TODO: A subagent has its own instruction file and a narrow job.
- TODO: Leave the detail with that agent. The parent instructions stay short.

## Commands

- TODO: A command is a named instruction a person invokes.
- TODO: Use one when the steps are the same each time and do not belong in the standing rules.

## What the agent may run

- TODO: Allow the commands the task needs, such as build and test, so a person does not confirm each one.
- TODO: Refuse a push, a change to production configuration, and any file that holds a secret.
- TODO: A sentence in an instruction file asks for that limit. The tool's deny list is what stops the command.

## Drift

An instruction file that contradicts the code will be followed unpredictably. Update the file or delete the rule.

## Window limits

A long conversation forgets the start. Start a new one when the task changes.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [Using MCP](/ai-assisted-development/using-mcp)
- [Building a SaaS: Project Setup](/building-a-saas/01-project-setup/overview)

---

**Next:** [Verification](/ai-assisted-development/verification)
