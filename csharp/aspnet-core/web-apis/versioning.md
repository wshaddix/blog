# API Versioning

How a contract changes without breaking a client you already shipped.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Changes that don't need a version

- TODO: A new field an existing client can ignore does not need a new version.
- TODO: Clients this product ships, including Uno and WinUI, keep working when a response gains a field they do not read.
- TODO: The point where a new version costs less than another compatible change is [What counts as a break](#what-counts-as-a-break).

## What counts as a break

Removing a field, changing a type, and changing an error code.

## URL and header versions

Where the version lives, and one choice per API.

## Supporting two versions

How long the old one stays, and who deletes it.

## Deprecating deliberately

- TODO: Name the field you will remove. Send `Deprecation` and `Sunset`, and link to the page that explains the replacement.
- TODO: Measure who still sends or reads the old shape before you delete it.
- TODO: Open a new version when one more compatible patch would cost more than carrying two contracts.
- TODO: The tenants still on the old field are [Who still calls a deprecated field](/building-a-saas/06-api-development/overview#who-still-calls-a-deprecated-field).

## Clients

Uno and WinUI builds in the field will call the old version.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [OpenAPI](/csharp/aspnet-core/web-apis/openapi)

---

**Next:** [Caching](/csharp/aspnet-core/web-apis/caching)
