---
title: bUnit
order: 40
---

# bUnit

[bUnit](https://bunit.dev) renders a Blazor component in memory. It runs on TUnit the same way any other test does.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## What it proves

Rendered markup, parameters, and an event handler. Not the API and not the database.

## A test

Render a component, find an element, and assert on the text or the markup.

## Services

Register a fake authentication state or a typed client the component injects.

## Razor tests and the source generator

bUnit supports TUnit. Razor test files and TUnit's source generator have not always seen each other's output. Confirm the current guidance on bunit.dev when this page is written, and record the workaround here if one is still required.

## What belongs in an API test instead

Status codes, persistence, and authorization.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Components and routing](/csharp/aspnet-core/blazor/components-and-routing)
- [TUnit project setup](/csharp/testing/project-setup)

---

**Next:** [Reqnroll](/csharp/testing/reqnroll/overview)
