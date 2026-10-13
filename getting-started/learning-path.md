# Suggested Learning Path

A roadmap through the material based on your experience level. Most pages are outlines. Each one will grow a C# sample, with a companion `.cs` file when the sample is longer than about 30 lines.

## Path 1: New to Software Engineering

**Duration:** 9-12 months (part-time)

This path ends when you can build a console app and a small API with authentication, authorization, Entity Framework, and tests. Web UI, Windows, mobile, MCP, and the SaaS project are Path 4.

### Phase 1: Workstation (Weeks 1-2)

1. [Prerequisites](/getting-started/prerequisites) - Verify you're ready
2. [Workstation Setup](/getting-started/workstation-setup) - Get your tools
3. [AI-Assisted Development](/ai-assisted-development/overview) - Terms and techniques you will use the rest of the way
4. [Git Installation](/devops/version-control/git-installation) - Version control on day one
5. [Branching and Pull Requests](/devops/version-control/branching-and-pull-requests) - How a change lands on `main`

### Phase 2: Foundations (Months 1-2)

1. [Big O](/fundamentals/algorithms/big-o-notation) - Start thinking about complexity
2. [Data Structures](/fundamentals/data-structures/arrays) - Arrays through trees
3. [OOP Principles](/fundamentals/programming-concepts/oop-principles) - Foundation for C#
4. [Error Handling](/fundamentals/programming-concepts/error-handling) - What a caller is owed when something fails
5. [HTTP and the Web](/fundamentals/networking/http) - Read this before any API
6. [Security Concepts](/fundamentals/security/overview) - The failures a feature developer meets
7. [Authentication and Authorization](/fundamentals/security/authentication-and-authorization) - Who the caller is, and what they may do

### Phase 3: C# (Months 3-4)

1. [Getting Started](/csharp/language-basics/getting-started) - Your first program
2. [Projects and Solutions](/csharp/language-basics/projects-and-solutions) - How a program is built
3. The rest of [Language Basics](/csharp/language-basics/getting-started) - Types, nullability, exceptions, collections, delegates, disposal
4. [LINQ](/csharp/advanced-features/linq) - Essential for productivity
5. [Async](/csharp/advanced-features/async) - Modern C# requirement

### Phase 4: The Platform, then a Console App (Month 5)

1. [The .NET Platform](/csharp/platform/overview) - Host, dependency injection, configuration, logging, HTTP clients
2. [Console Apps](/csharp/console/overview) - The smallest thing you can ship
3. [Command-Line Parsing](/csharp/console/command-line) - A real command

### Phase 5: Data (Months 5-6)

1. [SQL Fundamentals](/databases/relational/sql-fundamentals) - The language
2. [Indexes and Query Plans](/databases/relational/indexes-and-query-plans) - Why a query is fast or slow
3. [Transactions and Isolation](/databases/relational/transactions-and-isolation) - Atomic changes
4. [Entity Framework](/csharp/entity-framework/getting-started) - Then [modeling](/csharp/entity-framework/modeling), [change tracking](/csharp/entity-framework/change-tracking), and [transactions](/csharp/entity-framework/transactions)
5. [Repository](/patterns/application-patterns/repository) - And why `DbContext` is already a unit of work

### Phase 6: Tests (Month 6)

1. [Debugging](/sdlc/debugging) - Reproduce, narrow, fix, prove
2. [Testing Strategy](/sdlc/testing-strategy) - What each kind of test proves
3. [TUnit Project Setup](/csharp/testing/project-setup) - The runner this site uses
4. [Unit Testing](/csharp/testing/unit-testing) and [Mocking](/csharp/testing/mocking) - TUnit and TUnit.Mocks
5. [ASP.NET Core Tests](/csharp/testing/webapplicationfactory) - The API in-process
6. [Reqnroll](/csharp/testing/reqnroll/overview) - A feature file that runs as a TUnit test

### Phase 7: A Secured API (Months 7-10)

1. [Web APIs](/csharp/aspnet-core/web-apis/overview) - Endpoints, validation, errors, OpenAPI
2. [Choosing a Scheme](/csharp/aspnet-core/authentication/choosing-a-scheme) - Cookie, JWT, or OpenID Connect
3. [JWT](/csharp/aspnet-core/authentication/jwt) and [Authorization](/csharp/aspnet-core/authorization/overview) - Including a check against a specific row
4. [Rate Limiting](/csharp/aspnet-core/web-apis/rate-limiting) - Slow a caller down
5. [Observability](/csharp/aspnet-core/observability/overview) and [Health Checks](/csharp/aspnet-core/observability/health-checks) - Logs, traces, and a readiness probe
6. [Secrets](/csharp/security/secrets) and [Kestrel and HTTPS](/csharp/aspnet-core/hosting/kestrel-and-https) - Nothing secret in the repository, and TLS in front

### Phase 8: How the Work Is Done (Ongoing)

1. [Architecture](/sdlc/architecture) - Where each app type sits
2. [Code Review](/sdlc/code-review) - Including a review of generated code
3. [Verification](/ai-assisted-development/verification) - The assistant does not replace the diff

---

## Path 2: Experienced Developer, New to .NET

**Duration:** 3-5 months (part-time)

Same destination as Path 1: a console app and a secured API. Skip the foundations you already have. Use the [AI-assisted development](/ai-assisted-development/overview) section as you go.

### Phase 1: C# and the Platform (Weeks 1-3)

1. [Language Basics](/csharp/language-basics/getting-started) - Skim for syntax, then read [nullability](/csharp/language-basics/nullability) and [projects and solutions](/csharp/language-basics/projects-and-solutions)
2. [LINQ](/csharp/advanced-features/linq), [async](/csharp/advanced-features/async), and [records](/csharp/advanced-features/records)
3. [The .NET Platform](/csharp/platform/overview) - Host, dependency injection, configuration, logging, HTTP clients
4. [Console Apps](/csharp/console/overview) - One small tool

### Phase 2: Data and the API (Weeks 4-8)

1. [Entity Framework](/csharp/entity-framework/getting-started) - Modeling, change tracking, transactions
2. [Web APIs](/csharp/aspnet-core/web-apis/overview) - Including validation, Problem Details, and rate limiting
3. [Choosing a Scheme](/csharp/aspnet-core/authentication/choosing-a-scheme), [JWT](/csharp/aspnet-core/authentication/jwt), and [authorization](/csharp/aspnet-core/authorization/overview)
4. [Observability](/csharp/aspnet-core/observability/overview)

### Phase 3: Tests (Weeks 6-8, alongside the API)

1. [TUnit Project Setup](/csharp/testing/project-setup), [unit tests](/csharp/testing/unit-testing), and [mocks](/csharp/testing/mocking)
2. [ASP.NET Core tests](/csharp/testing/webapplicationfactory)
3. [Reqnroll](/csharp/testing/reqnroll/overview) - Scenarios on the TUnit runner

Continue with Path 4.

---

## Path 3: Senior Engineer → Management

**Duration:** Ongoing

### Immediate Focus

1. [Career Ladder](/career-development/career-ladder) - Understand the transition
2. [Individual Contributor → Manager](/career-development/career-ladder/individual-contributor) - Specific guidance
3. [One-on-Ones](/career-development/people-management/one-on-ones) - Your most important tool
4. [Giving Feedback](/career-development/people-management/feedback) - Practice immediately

### First 90 Days

1. [Hiring](/career-development/people-management/hiring) - If you're building a team
2. [Team Building](/career-development/people-management/team-building) - Culture matters
3. [Skill Matrices](/career-development/team-operations/skill-matrices) - Know your team

### Ongoing Development

1. [Stakeholder Management](/career-development/soft-skills/stakeholder-management) - Working with others
2. [Technical Writing](/career-development/soft-skills/technical-writing) - Clear communication
3. [Manager → Director](/career-development/career-ladder/director) - Next level

---

## Path 4: Full-Stack C# Applications

**Duration:** 6-9 months (part-time), after Path 1 or Path 2

The client rule for this path: the UI renders and calls the API. Business rules stay on the server.

### Web

1. [Blazor](/csharp/aspnet-core/blazor/overview) - Components, forms, and render modes
2. [Blazor authentication](/csharp/aspnet-core/blazor/authentication) - A cookie, not a token in the browser
3. [bUnit](/csharp/testing/bunit) - Component tests on TUnit

### Windows

1. [Clients](/csharp/clients/overview) - MVVM, XAML, and the shared API client
2. [WinUI 3](/csharp/winui/overview) - Windowing, packaging, and authentication

### Mobile and WebAssembly

1. [Uno Platform](/csharp/uno/overview) - Targets, platform-specific code, and device authentication

### MCP

1. [MCP Servers](/csharp/mcp/overview) - Tools, resources, and prompts
2. [Hosting](/csharp/mcp/hosting) - stdio for a local client, HTTP for a remote one
3. [Using MCP](/ai-assisted-development/using-mcp) - The client side of the same protocol

### Capstone

1. [Building a SaaS](/building-a-saas/overview) - The applied project. Its chapters link back to the reference pages.
2. [Redis](/databases/nosql/redis), [SignalR](/csharp/aspnet-core/web-apis/signalr), and [background services](/csharp/aspnet-core/web-apis/background-services) show up as the project needs them
3. [Patterns](/patterns/overview) - Reference while you build. [Decorator](/patterns/coding-patterns/decorator) and [CQRS](/patterns/application-patterns/cqrs) are the two taught beyond the repository

---

## How to Learn Effectively

1. **Don't just read** - Build things with what you learn
2. **Take notes** - In your own words
3. **Teach others** - Best way to solidify knowledge
4. **Be patient** - Mastery takes time
5. **Review generated code** - An assistant can draft a sample. You still read the diff and run the tests

---

*Pick the path that fits your situation and get started. You can always adjust as you go.*
