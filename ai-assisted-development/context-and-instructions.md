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

## Hooks

- TODO: A hook runs at a fixed moment, such as before a tool call or after a file write.
- TODO: Put a rule in a hook when it has to run every time, not only when the model remembers a file.

## Subagents

- TODO: A subagent has its own instruction file and a narrow job.
- TODO: Leave the detail with that agent. The parent instructions stay short.

## Commands

- TODO: A command is a named instruction a person invokes.
- TODO: Use one when the steps are the same each time and do not belong in the standing rules.

## Drift

An instruction file that contradicts the code will be followed unpredictably. Update the file or delete the rule.

## Window limits

A long conversation forgets the start. Start a new one when the task changes.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [Using MCP](/ai-assisted-development/using-mcp)

---

**Next:** [Verification](/ai-assisted-development/verification)
