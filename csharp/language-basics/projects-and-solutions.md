---
title: Projects and Solutions
order: 120
---

# Projects and Solutions

A solution is a set of projects. A project compiles to an assembly. This is the unit you build, reference, and ship.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Solutions and projects

`.sln` and `.csproj`. What `dotnet build` actually builds.

## SDKs

Microsoft.NET.Sdk, the web SDK, and what each one adds.

## Namespaces and assemblies

A namespace organizes types. An assembly is the file you deploy.

## Package references

NuGet, version ranges, and a lock on what you restored.

## Project references

Which project is allowed to see which other project.

## Target frameworks

One TFM, and what changes when a project multi-targets.

## Directory.Build.props

<!-- TODO: Language version, nullable, warnings as errors -->

## Central Package Management

<!-- TODO: Directory.Packages.props and transitive pinning -->

## EditorConfig and analyzers

<!-- TODO: .editorconfig, analyzers, and dotnet format in CI -->

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Getting started](/csharp/language-basics/getting-started)
- [.NET CLI](/tool-references/dotnet-cli)

---

**Next:** [Types and Variables](/csharp/language-basics/types)
