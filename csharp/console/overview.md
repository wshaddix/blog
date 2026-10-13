# Console Apps

A console app is the smallest host: configuration, logging, and a job that exits with a code.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The host

Build a generic host even when the program is a single command.

## Exit codes

Zero for success. A non-zero code the caller can branch on.

## stdin and stdout

Pipes, and why logging must not corrupt the data on stdout.

## Top-level statements

The implicit entry point, and when a named `Main` is clearer.

## Cancellation

`Ctrl+C` and `IHostApplicationLifetime`.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Generic host](/csharp/platform/generic-host)
- [Command-line parsing](/csharp/console/command-line)

---

**Next:** [Command-Line Parsing](/csharp/console/command-line)
