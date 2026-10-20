---
title: Overview
order: 1
---

# Chapter 1: Project Setup

A well-organized project structure sets the foundation for maintainability and scalability.

## What We'll Cover

- Solution and project structure
- Development environment setup
- Initial configuration
- Git repository setup
- CI pipeline foundation
- Directory.Build.props, central package management, and EditorConfig
- Aspire AppHost for local dependencies
- Target framework and upgrades
- Agent rules in the repo
- An automated review step

## Solution Structure

<!-- TODO: Multi-project solution, separation of concerns -->

## Development Environment

<!-- TODO: Required tools, VS Code / Visual Studio setup -->

## Configuration

<!-- TODO: appsettings.json, user secrets, environment variables -->

## Git Setup

<!-- TODO: .gitignore, branching strategy, initial commit -->

## Directory.Build.props

<!-- TODO: Language version, nullable, warnings as errors -->

## Central Package Management

<!-- TODO: Directory.Packages.props and transitive pinning -->

## EditorConfig

<!-- TODO: .editorconfig, analyzers, and dotnet format in CI -->

## Aspire AppHost

<!-- TODO: SQL, Redis, API, worker, and the dashboard -->

## Target framework and upgrades

- TODO: The solution targets the current LTS. Try a newer release candidate on a branch, and ship the framework the product has chosen.
- TODO: Write down what an upgrade re-tests before the target framework changes.

## Agent rules in the repo

- TODO: Keep the rules the agent follows in the repository: a short root file, a file beside the code it governs, and hooks that run even when the model skips a file.
- TODO: A hook formats after an edit, runs the tests before the task is called done, and blocks edits to the tests when the task is to make those tests pass.
- TODO: A folder file holds the rules for that folder. The root file stays short enough that a person will still read it.

## Automated review step

- TODO: Run the agent with no chat, from a git hook or from the pipeline, and give it the diff to review.
- TODO: The step comments on the change. Merging stays with the person who reviews it.

## Related Topics

- See [Projects and Solutions](/csharp/language-basics/projects-and-solutions)
- See [.NET Aspire](/csharp/platform/aspire)
- See [Modern C#](/csharp/advanced-features/modern-csharp)
- See [Context and instructions](/ai-assisted-development/context-and-instructions)
- See [Tools](/ai-assisted-development/tools)
- See [CI/CD concepts](/devops/ci-cd/concepts)

---

**Next:** [Chapter 2: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview)
