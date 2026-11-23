---
title: Blazor
order: 60
---

# Blazor

Blazor is the C# web UI. It talks to the API. It does not become a second place where business rules live.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## In this section

- [Components and routing](/csharp/aspnet-core/blazor/components-and-routing) - Components, parameters, and the router.
- [Data grids](/csharp/aspnet-core/blazor/data-grids) - A grid that shows one page of rows from the API.
- [Forms and validation](/csharp/aspnet-core/blazor/forms-and-validation) - Editing data and showing field errors.
- [Authentication](/csharp/aspnet-core/blazor/authentication) - Cookies, AuthorizeView, and the token the browser must not hold.
- [Calling the API](/csharp/aspnet-core/blazor/calling-the-api) - A typed client from a component.
- [AI features](/csharp/aspnet-core/blazor/ai-features) - A component that shows a model's answer. The prompt stays on the server.
- [JavaScript interop](/csharp/aspnet-core/blazor/javascript-interop) - Calling browser APIs from C#.

## Render modes

Static, interactive server, WebAssembly, and auto. What runs where.

## Prerendering and persisted state

- TODO: A prerendered component loads its data, then loads it again when the interactive circuit starts.
- TODO: Persist the first result and reuse it, so the second pass does not fetch.
- TODO: Do not persist a secret, and do not persist a list large enough to bloat the page.
- TODO: Cover both passes with bUnit. See [bUnit](/csharp/testing/bunit).
- TODO: The same double load on a long-running request is [Loading the same data twice](/building-a-saas/06-api-development/overview#loading-the-same-data-twice).

## The host

A Blazor app is an ASP.NET Core app with a component model.

## Auth

Cookies for the browser. See the authentication page in this section.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)

---

**Next:** [Components and Routing](/csharp/aspnet-core/blazor/components-and-routing)
