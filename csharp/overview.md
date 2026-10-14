# C# and .NET

C# is a modern, object-oriented programming language developed by Microsoft. Combined with the .NET platform, it's one of the most versatile ecosystems for building applications.

## Why C#?

- **Versatile:** Build web apps, APIs, desktop apps, mobile apps, games, cloud services
- **Modern features:** Async/await, LINQ, pattern matching, records
- **Strong typing:** Catch errors at compile time
- **Great tooling:** Visual Studio, VS Code, JetBrains Rider
- **Enterprise-ready:** Used by countless businesses for production systems
- **Active development:** Regular language updates with new features

## What's Covered

### Language Basics

The foundation - syntax, types, and core features:

- [Getting Started](/csharp/language-basics/getting-started) - Your first C# program
- [Types and Variables](/csharp/language-basics/types) - Value types, reference types, nullability
- [Control Flow](/csharp/language-basics/control-flow) - Conditions, loops, branching
- [Methods and Parameters](/csharp/language-basics/methods) - Functions, parameters, returns
- [Classes and Objects](/csharp/language-basics/classes) - OOP in C#
- [Collections](/csharp/language-basics/collections) - Lists, dictionaries, arrays

### Advanced Features

Taking your C# skills to the next level:

- [Generics](/csharp/advanced-features/generics) - Type-safe reusable code
- [LINQ](/csharp/advanced-features/linq) - Query syntax for collections
- [Async/Await](/csharp/advanced-features/async) - Asynchronous programming
- [Cancellation](/csharp/advanced-features/cancellation) - Tokens and bounded concurrency
- [Records and Init](/csharp/advanced-features/records) - Immutable data types
- [Pattern Matching](/csharp/advanced-features/pattern-matching) - Declarative conditionals
- [High-Performance C#](/csharp/advanced-features/high-performance-csharp) - Primitives for hot paths
- [Attributes](/csharp/advanced-features/attributes) - Metadata for validation and tools
- [Modern C#](/csharp/advanced-features/modern-csharp) - The dialect current .NET code uses

### The Platform

Shared by every app type on this site:

- [Overview](/csharp/platform/overview) - Host, services, configuration, logging, HTTP
- [Console apps](/csharp/console/overview) - The smallest host

### Entity Framework Core

Microsoft's ORM for database access:

- [Getting Started](/csharp/entity-framework/getting-started) - Setup and configuration
- [DbContext](/csharp/entity-framework/dbcontext) - The unit of work
- [Modeling](/csharp/entity-framework/modeling) - Relationships, owned types, conversions
- [Querying](/csharp/entity-framework/querying) - LINQ to SQL
- [Change Tracking](/csharp/entity-framework/change-tracking) - What `SaveChanges` writes
- [Migrations](/csharp/entity-framework/migrations) - Database schema evolution
- [Transactions](/csharp/entity-framework/transactions) - More than one save, one commit
- [Concurrency](/csharp/entity-framework/concurrency) - Lost updates, tokens, and atomic counters
- [Performance](/csharp/entity-framework/performance) - Avoiding common pitfalls
- [Testing](/csharp/entity-framework/testing) - Relational tests, not the in-memory provider

### ASP.NET Core

Building web applications and APIs:

- [Web APIs](/csharp/aspnet-core/web-apis/overview) - HTTP APIs, validation, rate limiting, OpenAPI
- [Authentication](/csharp/aspnet-core/authentication/overview) - Cookies, JWT, OpenID Connect
- [Authorization](/csharp/aspnet-core/authorization/overview) - Roles, permissions, policies, and a specific row
- [Middleware](/csharp/aspnet-core/middleware/overview) - Request pipeline
- [Blazor](/csharp/aspnet-core/blazor/overview) - The C# web UI
- [Observability](/csharp/aspnet-core/observability/overview) - Logs, metrics, and traces

### Clients

- [Shared client code](/csharp/clients/overview) - MVVM, XAML, and the API client
- [WinUI 3](/csharp/winui/overview) - Native Windows
- [Uno Platform](/csharp/uno/overview) - iOS, Android, WebAssembly, and desktop
- [MCP servers](/csharp/mcp/overview) - Clients, tools, resources, and prompts for an AI client

### Security

- [Secrets, log redaction, transport, and data protection](/csharp/security/overview)

### Testing

TUnit is the runner. Reqnroll runs behavior scenarios on that same runner.

- [Project setup](/csharp/testing/project-setup) - A TUnit executable
- [Unit Testing](/csharp/testing/unit-testing) - `[Test]` and `Assert.That`
- [Mocking](/csharp/testing/mocking) - TUnit.Mocks
- [Time-dependent code](/csharp/testing/time-dependent-code) - A clock the test controls
- [Integration Testing](/csharp/testing/integration-testing) - The API and a real database
- [Reqnroll](/csharp/testing/reqnroll/overview) - Gherkin features

## Learning Path

If you're new to C#:

1. Start with [Language Basics](/csharp/language-basics/getting-started) - master the syntax
2. Practice with [Fundamentals exercises](/fundamentals/overview) - implement data structures
3. Learn [LINQ](/csharp/advanced-features/linq) - essential for productive C#
4. Build a [console app](/csharp/console/overview), then an [API](/csharp/aspnet-core/web-apis/overview)
5. Apply everything in [Building a SaaS](/building-a-saas/overview) - comprehensive project

The full sequence, including WinUI, Uno, and MCP, is the [learning path](/getting-started/learning-path).

Code samples land on the page. A sample longer than about 30 lines goes in a companion `.cs` file next to that page.

---

*New to C#? Start with [Getting Started](/csharp/language-basics/getting-started).*
