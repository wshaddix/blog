---
title: Conventional Commits
icon: comment
layout: default
---

[Conventional Commits](https://www.conventionalcommits.org/) is specification for adding human and machine readable meaning to commit messages.

## Commit Message Structure

```
<type>[optional scope]: <description>

[optional body]

[optional footer]
```

## Commit Types

| Commit Type | Description                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `build`     | Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)             |
| `ci`        | Changes to CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)         |
| `chore`     | Changes which doesn't change source code or tests e.g. changes to the build process, auxiliary tools, libraries |
| `docs`      | Documentation only changes                                                                                      |
| `feat`      | A new feature                                                                                                   |
| `fix`       | A bug fix                                                                                                       |
| `perf`      | A code change that improves performance                                                                         |
| `refactor`  | A code change that neither fixes a bug nor adds a feature                                                       |
| `revert`    | Revert something                                                                                                |
| `style`     | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)          |
| `test`      | Adding missing tests or correcting existing tests                                                               |

## Examples

```text
feat: add jwt support
feat!: breaking change in API
feat!(ui): redesign user profile page
fix: fix SQL injection vulnerability
fix(database): resolve data race condition
docs: update setup section of README
style(login): correct indentation in login component
refactor: refactor user database schema
perf: optimize user retrieval code for faster response
test: add tests for jwt authentication
test(payment): add tests for the payment gateway
chore: update build script
chore(deps): update dependencies
build(docker): update Dockerfile to use node 14
ci: add job for integration tests
revert: revert commit a1b2c3d4e5f
```

## Specification

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

1. Commits MUST be prefixed with a type, which consists of a noun, feat, fix, etc., followed by a colon and a space.

2. The type feat MUST be used when a commit adds a new feature to your application or library.

3. The type fix MUST be used when a commit represents a bug fix for your application.

4. An optional scope MAY be provided after a type. A scope is a phrase describing a section of the codebase enclosed in parenthesis, e.g., fix(parser):

5. A description MUST immediately follow the type/scope prefix. The description is a short description of the code changes, e.g., fix: array parsing issue when multiple spaces were contained in string.

6. A longer commit body MAY be provided after the short description, providing additional contextual information about the code changes. The body MUST begin one blank line after the description.

7. A footer MAY be provided one blank line after the body. The footer SHOULD contain additional issue references about the code changes (such as the issues it fixes, e.g., Fixes #13).

8. Breaking changes MUST be indicated in the footer AND by appending a ! after the type/scope. A BREAKING CHANGE introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type.

9. A description MUST be provided after the BREAKING CHANGE:, describing what has changed about the API, e.g., BREAKING CHANGE: environment variables now take precedence over config files.

10. The footer MUST only contain BREAKING CHANGE, external links, issue references, and other meta-information.

11. Types other than feat and fix MAY be used in your commit messages.
