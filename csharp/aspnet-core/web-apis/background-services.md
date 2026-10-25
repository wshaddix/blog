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

## Quartz

## More than one instance

- TODO: A lock inside the process only covers that process. A second instance has its own lock and can start the same scheduled job.
- TODO: Have every instance try one lock that lives outside the app, such as a PostgreSQL advisory lock. The instance that does not get the lock skips the run.
- TODO: That lock lasts while its database connection holds it. A dropped connection lets another instance take the lock while work is still in flight.
- TODO: Record the runs that finished. The lock does not, and a repeat of the same run has to be safe.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Generic host](/csharp/platform/generic-host)
- [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview)

---

**Next:** [gRPC](/csharp/aspnet-core/web-apis/grpc)
