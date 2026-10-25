# Publishing

How a project becomes a program you can run on another machine.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Framework-dependent and self-contained

Who has to install the runtime.

## Single file

One executable, and what is still unpacked beside it.

## Runtime identifier

Win-x64, linux-x64, and the other RIDs.

## Trimming and AOT

What native compilation demands of your code. Relevant to console tools and Uno.

### AOT versus JIT

- TODO: JIT compiles methods as they run and can use the full runtime, including reflection and generated code.
- TODO: AOT compiles ahead of publish. Startup is shorter and the output is native code, and the publish takes longer.

### Workloads that suit AOT

- TODO: Short-lived tools, CLI apps, and small services that care about startup time and a smaller deployable are a strong fit for AOT.
- TODO: A long-running API that depends on runtime code generation or plugins is a strong fit for JIT.

### What breaks under trimming

- TODO: Trimming removes code it cannot see is used. Reflection, serializers that bind by name, and types loaded from a string are the usual losses.
- TODO: A trim warning names a member that may be missing when the process runs. Preserve it when a real runtime path needs it.

## Configuration at publish time

What is baked in, and what is still read from the environment.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Projects and solutions](/csharp/language-basics/projects-and-solutions)

---

**Next:** [Console Apps](/csharp/console/overview)
