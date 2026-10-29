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

## Development Environment

## Configuration

## Git Setup

## Directory.Build.props

## Central Package Management

## EditorConfig

## Aspire AppHost

### A local model as a dev resource

- TODO: The AppHost starts a model on the developer machine and passes its address to the API, next to SQL and Redis.
- TODO: The API reads that address from configuration. Production points the same setting at the hosted model, as in [A local model in development](/csharp/mcp/clients-and-agents#a-local-model-in-development).

## Target framework and upgrades

- TODO: The solution targets the current LTS. Try a newer release candidate on a branch, and ship the framework the product has chosen.
- TODO: Write down what an upgrade re-tests before the target framework changes.

### When the target loses support

- TODO: Plan the move off a target framework before its support window closes, and confirm the date on Microsoft's support policy page before you schedule the work.
- TODO: Follow the upgrade order in [Support windows and end of support](/csharp/platform/publishing#support-windows-and-end-of-support), including a fresh publish of every self-contained deploy.

## Agent rules in the repo

- TODO: Keep the rules the agent follows in the repository: a short root file, a file beside the code it governs, and hooks that run even when the model skips a file.
- TODO: A hook formats after an edit, runs the tests before the task is called done, and blocks edits to the tests when the task is to make those tests pass.
- TODO: A folder file holds the rules for that folder. The root file stays short enough that a person will still read it.

### Allowed and denied commands

- TODO: The rules name the commands an agent may run without asking, and the commands that are refused.
- TODO: Build and test are allowed. A push, production settings, and secret files are denied.
- TODO: The deny is enforced by the tool. A sentence in the instruction file is not the only control.

## Automated review step

- TODO: Run the agent with no chat, from a git hook or from the pipeline, and give it the diff to review.
- TODO: The step comments on the change. Merging stays with the person who reviews it.

### A check that can block a commit

- TODO: The hook can fail the commit, not only comment later on a pull request.
- TODO: A secret in the diff stops the commit. A check that did not run stops it as well. A clean commit still waits for a person before it merges.
- TODO: The hook is [Blocking a commit](/ai-assisted-development/tools#blocking-a-commit), and the secret scan is [Before it reaches the repo](/ai-assisted-development/risks-and-limits#before-it-reaches-the-repo).

## Related Topics

- See [Projects and Solutions](/csharp/language-basics/projects-and-solutions)
- See [.NET Aspire](/csharp/platform/aspire)
- See [Modern C#](/csharp/advanced-features/modern-csharp)
- See [Context and instructions](/ai-assisted-development/context-and-instructions)
- See [Tools](/ai-assisted-development/tools)
- See [CI/CD concepts](/devops/ci-cd/concepts)

---

**Next:** [Chapter 2: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview)
