---
title: Publishing
order: 10
---

# Publishing

How a project becomes a program you can run on another machine.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Framework-dependent and self-contained

Who has to install the runtime.

### Who patches the runtime

- TODO: Who ships a runtime security fix for a framework-dependent deploy and for a self-contained deploy. See [Rebuilding for runtime patches](/building-a-saas/11-deployment/overview#rebuilding-for-runtime-patches).

## Support windows and end of support

- TODO: A long-term support release and a standard-term support release are serviced for different lengths of time. Read the current lengths and the end dates on Microsoft's support policy page, and fill this section from that page.
- TODO: When support ends, servicing for that runtime stops. List every target framework, the SDK pin in `global.json`, and each container base image so you can see which deploys are still on it.
- TODO: Upgrade the SDK, then the target framework, then the packages, and run the full test suite before the change ships.
- TODO: Publish self-contained builds again and redeploy them, so those hosts pick up the runtime you just moved to. See [When the target loses support](/building-a-saas/01-project-setup/overview#when-the-target-loses-support).

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
