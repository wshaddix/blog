---
title: Overview
order: 1
---

# Chapter 8: Background Jobs

Not everything should happen in the request/response cycle. Background jobs handle async work.

## What We'll Cover

- When to use background jobs
- In-process vs out-of-process
- Hangfire setup and usage
- Azure Functions for serverless jobs
- Scheduled jobs
- Error handling and retries

## When to Use Background Jobs

- Email sending
- Report generation
- Data imports/exports
- Scheduled maintenance
- Webhook processing

### Notification jobs

- TODO: A job that notifies many people reads a large set of rows, then waits on the mail or push provider.
- TODO: Count the queries that read that set, and walk the rows once.
- TODO: Release the database reader before the await that sends the notification, so a slow provider leaves the connection free.

## Job Processing Options

| Option | Pros | Cons |
|--------|------|------|
| Hosted Service | Simple, in-process | Tied to web app lifecycle |
| Hangfire | Full-featured, dashboard | Additional complexity |
| Azure Functions | Serverless, scalable | Cold starts, deployment |

## Implementation

<!-- TODO: Job creation, scheduling, monitoring -->

## Error Handling

<!-- TODO: Retries, dead letter, alerting -->

## Reliable messaging

<!-- TODO: Publish domain events through an outbox -->

## Shutdown and cancellation

<!-- TODO: The host stops, and in-flight work honors the token -->

## One run across instances

- TODO: A schedule that is registered on every instance will fire on every instance. Take one shared lock before the job body runs.
- TODO: Hold the lock on a connection that stays open for the work. If that connection drops, another instance may take the lock while the first is still running, so the rest of the run has to be safe to repeat.
- TODO: Record which occurrence finished. The lock does not remember that, and a later instance must not do the same occurrence again.

## When a saga needs a person

<!-- TODO: Compensation that fails, and a parked state someone has to resolve -->

## Workflows that wait

- TODO: A trial end, a dunning sequence, and an approval are waits. Each one stores a deadline and the path to take when nobody answers in time.
- TODO: The deadline is part of the workflow record, so a restart keeps it and runs the timeout path once.

## A context in a background worker

- TODO: A job has no HTTP request, so it has no request-scoped context.
- TODO: Open a scope for that job, use a context from the scope, and dispose the scope before the next job starts.

## Related Topics

- See [Azure Functions](/devops/azure/functions)
- See [Fundamentals: Concurrency](/fundamentals/programming-concepts/concurrency)
- See [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)
- See [Background services](/csharp/aspnet-core/web-apis/background-services)
- See [DbContext](/csharp/entity-framework/dbcontext)
- See [Entity Framework performance](/csharp/entity-framework/performance)
- See [Sagas](/patterns/integration-patterns/sagas)
- See [Durable workflows](/patterns/integration-patterns/durable-workflows)

---

**Next:** [Chapter 9: Billing Integration](/building-a-saas/09-billing-integration/overview)
