---
title: Risks and Limits
order: 20
---

# Risks and Limits

The failure modes that show up in a team that uses assistants every day.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Secrets

A prompt, a log, and a pasted config file are copies of the secret.

### Before it reaches the repo

- TODO: Scan the staged diff for a key, a connection string, or a token before the commit is stored.
- TODO: A match blocks the commit. A scan that does not finish blocks it too. A skipped check is not a pass.
- TODO: The hook that applies this rule is [Blocking a commit](/ai-assisted-development/tools#blocking-a-commit).

## Licenses and provenance

Generated code can resemble code the model was trained on. You still publish it under your license.

## Confident errors

APIs, flags, and version numbers are often invented. Check them against the current docs.

## Over-reliance

Accepting a suggestion you cannot explain. The review page is the countermeasure.

## Privacy

What leaves the machine, and which product setting controls it.

## Instructions hidden in data

- TODO: A document, a ticket, or a tool result can contain a sentence that is written as an instruction.
- TODO: That sentence does not widen the task, change the recipient, or add a tool.
- TODO: When you review a run, look for a tool argument that was taken from that untrusted text.

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [Secrets](/csharp/security/secrets)
- [Verification](/ai-assisted-development/verification)

---

**Next:** [AI-Assisted Development](/ai-assisted-development/overview)
