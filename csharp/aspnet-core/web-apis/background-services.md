# Background Services

Work that must finish even though the HTTP request already returned.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## IHostedService

A loop in the same process as the API.

## Channels

A request hands work to the loop through a channel.

## What the process owes you

A restart loses in-memory work. Know when that is acceptable.

## A real queue

When the work has to survive a deploy. Hangfire and Functions stay in the SaaS chapter.

## Cancellation

Stopping the host stops the loop.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Generic host](/csharp/platform/generic-host)
- [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview)

---

**Next:** [SignalR](/csharp/aspnet-core/web-apis/signalr)
