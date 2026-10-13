---
title: Testing Strategy
order: 60
---

# Testing Strategy

What a unit test, an API test, a component test, and a scenario each prove. The runner for all of them on this site is TUnit.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The pyramid

Many small tests, fewer tests that boot the app, a handful that drive a full journey.

## What each layer owns

Domain rules, HTTP behavior, Blazor components, and XAML clients.

## What not to mock

The thing the test claims to prove.

## Scenarios

Reqnroll features for behavior a product owner can read.

## Speed and isolation

Parallel by default, and the shared resources that must opt out.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [TUnit project setup](/csharp/testing/project-setup)
- [Reqnroll](/csharp/testing/reqnroll/overview)
- [Building a SaaS: Testing](/building-a-saas/10-testing-strategy/overview)

---

**Next:** [Code Review](/sdlc/code-review)
