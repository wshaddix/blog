# AI Agent Instructions

This file contains guidelines for AI agents working with this software engineering knowledge base and codebase.

## Repository Overview

This is a comprehensive software engineering knowledge base covering:
- **Computer Science Fundamentals** - Data structures, algorithms, programming concepts
- **C# and .NET** - Language features, Entity Framework, ASP.NET Core, testing
- **Databases** - Relational and NoSQL, data modeling
- **Design Patterns** - GoF patterns, application patterns, integration patterns
- **DevOps** - Version control, CI/CD, containers, Azure, monitoring
- **SDLC** - Software development lifecycle
- **Building a SaaS** - 12-chapter comprehensive project walkthrough
- **Career Development** - Career ladder, people management, team operations, soft skills
- **Tool References** - Quick reference guides

## Technology Stack

- **Backend:** ASP.NET Core 8, C#
- **Database:** SQL Server / Azure SQL, Entity Framework Core
- **Cloud:** Azure (App Service, Functions, SQL)
- **Documentation:** Retype static site generator
- **Version Control:** Git with conventional commits
- **CI/CD:** GitHub Actions
- **Package Management:** NuGet, .NET CLI

## Working with This Codebase

### Guidelines

#### Testing
- Use `retype start` to preview documentation locally before deploying
- For code changes, build and test locally first: `dotnet build` and `dotnet test`
- The solution uses standard .NET project structure with multiple projects
- Tests use xUnit framework with Moq for mocking

#### Code Style
- Follow existing C# conventions seen in the codebase
- Use meaningful variable and method names
- Add appropriate XML documentation comments
- Keep PR descriptions clear and concise

#### Project Structure
```
/
├── getting-started/           # New user onboarding
├── fundamentals/              # CS theory
├── csharp/                   # Language and framework specific content
├── databases/                 # Database theory and practice
├── patterns/                  # Design patterns
├── sdlc/                      # Software development lifecycle
├── devops/                    # Operations and deployment
├── building-a-saas/           # Comprehensive project walkthrough
├── career-development/          # Leadership and management
├── tool-references/            # Quick reference guides
├── blog/                      # Personal posts
└── static/                     # Images and assets
```

### Available Commands

#### Testing and Building
```bash
# Build solution
dotnet build

# Run tests
dotnet test

# Run specific project tests
dotnet test ./MyProject.Tests

# Create new project
dotnet new webapi MyProject

# Add package
dotnet add package PackageName

# Run Retype locally
retype start

# Build and publish
dotnet publish -c Release
```

#### Documentation Generation
```bash
# Serve documentation locally
retype serve

# Generate with specific output format
retype build --output-dir ./dist --format html

# Create new documentation page
retype new <title> path/to/file.md
```

### Key Sections to Understand

#### For Documentation/Content Work
- **Fundamentals** section (`/fundamentals/overview.md`) - CS theory that underpins everything
- **C# section** (`/csharp/overview.md`) - Core language and .NET ecosystem
- **Building a SaaS** (`/building-a-saas/overview.md`) - 12-chapter practical project
- **Career Development** (`/career-development/overview.md`) - Leadership and management topics

#### For Code Development
- **Entity Framework** (`/csharp/entity-framework/`) - ORM patterns and usage
- **ASP.NET Core** (`/csharp/aspnet-core/`) - Web framework and APIs
- **DevOps tools** (`/devops/version-control/git-installation`, `devops/containerization/docker-fundamentals`) - Git, Docker, deployment

### Important Considerations

#### Dependencies and Packages
- Check `*.csproj` files for package references
- Use NuGet for third-party dependencies
- Prefer Microsoft packages for .NET ecosystem
- Update packages regularly

#### Security Best Practices
- Never commit secrets or API keys
- Use parameterized queries for Entity Framework
- Implement proper authentication and authorization
- Follow OWASP security guidelines

#### Performance Considerations
- Entity Framework Core: Use AsNoTracking() for read-only operations
- ASP.NET Core: Implement proper caching strategies
- Consider async/await for I/O operations
- Monitor application performance metrics

### Common Workflows

#### Adding New Content
1. Create new `.md` file with appropriate frontmatter
2. Add to relevant section's `index.yml` if needed
3. Run `retype start` to validate links and formatting
4. Consider adding cross-references to related sections

#### Fixing Issues
1. Run `retype build` to identify broken links
2. Check navigation ordering in `index.yml` files
3. Ensure proper Retype frontmatter format
4. Test locally before deploying changes

#### Code Examples
When adding code examples:
- Use proper using statements
- Include necessary error handling
- Add explanatory comments for complex code
- Ensure examples compile and run

### Git Workflow

This repository follows conventional commits:
- `feat:` - New features
- `fix:` - Bug fixes  
- `docs:` - Documentation changes
- `refactor:` - Code refactoring
- `test:` - Adding or updating tests

Branch structure follows `main` as primary branch with feature branches for development.

### Local Development Setup

1. Clone repository: `git clone <url>`
2. Install .NET SDK (latest LTS recommended)
3. Use VS Code or Visual Studio for development
4. Install Retype CLI: `npm install -g retypeapp/retype`
5. Run `retype start` for local development

## Examples of Good AI Agent Work

### Adding Documentation
✅ Create clear, structured markdown with proper frontmatter
✅ Add cross-references between related sections
✅ Include code examples when appropriate
✅ Follow established patterns and conventions
✅ Test documentation builds without warnings

### Code Modifications  
✅ Understand existing patterns before making changes
✅ Maintain backward compatibility
✅ Add appropriate tests for new features
✅ Update documentation to match code changes
✅ Consider performance implications

### Problem Analysis
✅ Analyze issues comprehensively before proposing solutions
✅ Consider both short-term fixes and long-term improvements
✅ Suggest architectural improvements when appropriate
✅ Provide multiple solution approaches with trade-offs

### Testing and Validation
✅ Run local tests before submitting changes
✅ Validate documentation builds correctly
✅ Test edge cases and error conditions
✅ Consider performance impact of changes
✅ Verify links and navigation work properly

## Prohibited Activities

❌ Do not commit secrets, API keys, or sensitive data
❌ Do not modify published URLs or links without reason
❌ Do not bypass security controls or ignore authentication
❌ Do not make breaking changes without proper versioning
❌ Do not commit without running local tests first

## Getting Help

For questions about this repository:
- Check existing documentation in relevant sections first
- Look at similar patterns in the codebase
- Consider the overall architecture and style
- When in doubt, ask for clarification about the specific task

## Notes

This is an educational repository focused on sharing software engineering knowledge. When working with this codebase, prioritize clarity, maintainability, and educational value over clever or complex solutions.

Documentation should be written clearly, with practical examples, and should cater to developers at all skill levels from beginners to advanced practitioners.