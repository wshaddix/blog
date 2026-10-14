---
title: HTTP Clients
order: 20
---

# HTTP Clients

One way to call HTTP from a console app, an API, Blazor, WinUI, Uno, and an MCP server.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## IHttpClientFactory

Why a shared `new HttpClient()` is the wrong default.

## Typed clients

A class that wraps one downstream API.

## Named versus typed clients

<!-- TODO: When to pick each -->

## Resilience pipelines

<!-- TODO: Microsoft.Extensions.Http.Resilience -->

### Standard handler

<!-- TODO: What the standard handler bundles -->

### Total timeout, per-attempt timeout, jitter, and the circuit breaker

<!-- TODO -->

## What must not be retried

<!-- TODO: Non-idempotent POSTs without keys -->

## Polly licensing

<!-- TODO: Check current terms before choosing a package -->

## Testing resilience

<!-- TODO: Fault injection with a fake handler -->

## Timeouts

A timeout on the client, and a timeout that cancels the attempt.

## Retries and circuit breakers

Transient failures, and the failures you do not retry.

## Auth handlers

A `DelegatingHandler` that attaches a bearer token.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Client HTTP and auth](/csharp/clients/http-and-auth)
- [Idempotent requests](/csharp/aspnet-core/web-apis/idempotent-requests)
- [Resilience in the API](/csharp/aspnet-core/web-apis/overview)

---

**Next:** [Publishing](/csharp/platform/publishing)
