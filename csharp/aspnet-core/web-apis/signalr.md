---
title: SignalR
order: 100
---

# SignalR

A persistent connection so the server can push a message to a Blazor, WinUI, or Uno client.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Hubs

A hub method the client calls, and a method the server calls on the client.

## Groups

A tenant, a user, or a document.

## Auth

The same identity as the API. A connection without a user is anonymous.

## Scale-out

One server holds the connection. A backplane when there are many servers.

## Clients

The .NET client shared by WinUI and Uno, and the Blazor client.

## Batching and backpressure

<!-- TODO: Sending in batches, and what happens when a client falls behind -->

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Authorization](/csharp/aspnet-core/authorization/overview)

---

**Next:** [Polling, Server-Sent Events, and Async Request-Reply](/csharp/aspnet-core/web-apis/polling-sse-and-async-request-reply)
