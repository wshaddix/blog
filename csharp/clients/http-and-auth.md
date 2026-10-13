---
title: HTTP and Auth
order: 30
---

# HTTP and Auth

A WinUI or Uno client calls the API with a typed client and attaches a bearer token.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Typed client

The same `IHttpClientFactory` registration as the platform page.

## The handler

A `DelegatingHandler` that adds the Authorization header and refreshes once on a 401.

## Problem Details

Read the error document. Do not show a raw stack to the user.

## Token storage

Secure storage. The view model never sees the raw refresh token if a handler can own it.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [HTTP clients](/csharp/platform/http-clients)
- [Refresh tokens](/csharp/aspnet-core/authentication/refresh-tokens)
- [OpenID Connect](/csharp/aspnet-core/authentication/openid-connect)

---

**Next:** [Navigation and Storage](/csharp/clients/navigation-and-storage)
