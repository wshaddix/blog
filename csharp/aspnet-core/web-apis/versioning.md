# API Versioning

How a contract changes without breaking a client you already shipped.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## What counts as a break

Removing a field, changing a type, and changing an error code.

## URL and header versions

Where the version lives, and one choice per API.

## Supporting two versions

How long the old one stays, and who deletes it.

## Clients

Uno and WinUI builds in the field will call the old version.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [OpenAPI](/csharp/aspnet-core/web-apis/openapi)

---

**Next:** [Caching](/csharp/aspnet-core/web-apis/caching)
