# Modern C#

Language features you will see in current .NET code. Each one is small. Together they are the dialect this site uses.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## File-scoped namespaces and global usings

Less ceremony at the top of a file.

## Records and required members

A reminder of records, plus `required` on a property that must be set.

## Primary constructors

Constructor parameters in scope for the whole type.

## Collection expressions

A single syntax for creating lists, spans, and arrays.

## Pattern matching recap

Where the pattern-matching page goes deeper.

## Unions and closed hierarchies

### Unions on hot paths

- TODO: A union can stand in for a result type, or for a library that boxes every case.
- TODO: Measure a value-type case against a reference case with BenchmarkDotNet before a union sits on a hot path. Allocations are the signal that a case was boxed.
- TODO: Keep a closed record hierarchy when the cases are large, or when callers already share that type.
- TODO: The language feature arrives with the framework bump in [Moving from 10 to 11](/building-a-saas/01-project-setup/overview#moving-from-10-to-11). Mapping the cases onto HTTP status codes is [Known failures](/csharp/aspnet-core/web-apis/error-handling#known-failures).

## Result-style errors

## .NET 8, 10, and 11

### .NET 11

- TODO: This is a release the site can target once the product chooses it. Read the release notes, and keep the solution on the version it ships.
- TODO: List which language and library changes from this release the site adopts, and which ones it leaves.
- TODO: The checklist for moving a solution from 10 to 11 is [Moving from 10 to 11](/building-a-saas/01-project-setup/overview#moving-from-10-to-11). What the authentication stack changed is [What changed in .NET 11](/csharp/aspnet-core/authentication/overview#what-changed-in-net-11).

### Async handled by the runtime

The compiler builds a state machine for an async method today. A later runtime may take that work on itself.

- TODO: Describe what that compiler-generated state machine does for an async method on the releases this site ships.
- TODO: Describe what changes when the runtime owns that machinery. Check the wording against the official .NET 11 release notes before this section is written.
- TODO: List the measurements to take on the same workload before the change and after it.
- TODO: List which call sites still need an edit, and which ones keep compiling as they are. See [What an upgrade gives for free](/building-a-saas/01-project-setup/overview#what-an-upgrade-gives-for-free).

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Records](/csharp/advanced-features/records)
- [Pattern matching](/csharp/advanced-features/pattern-matching)
- [Building a SaaS: Project Setup](/building-a-saas/01-project-setup/overview)

---

**Next:** [Attributes](/csharp/advanced-features/attributes)
