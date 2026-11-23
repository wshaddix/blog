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

### One job per channel

- TODO: One job that sends email, SMS, and push will retry all three when one of them fails.
- TODO: Fan out so each channel is its own job.
- TODO: Store a delivery record per channel. A retry skips a channel that already succeeded.
- TODO: Keep a dead letter per channel, and alert on that channel.

## Work queued for a user

- TODO: Store who enqueued the job and what they were allowed to do. Check again at execution, and skip the action when the permission is gone. See [Acting on a user's behalf later](/csharp/aspnet-core/web-apis/background-services#acting-on-a-users-behalf-later).

## Job Processing Options

| Option | Pros | Cons |
|--------|------|------|
| Hosted Service | Simple, in-process | Tied to web app lifecycle |
| Hangfire | Full-featured, dashboard | Additional complexity |
| Azure Functions | Serverless, scalable | Cold starts, deployment |

### A broker instead of a table

- TODO: Move off a database-table queue when a lightweight broker gives you a durable stream without that load on the application database. See [An external job queue](/csharp/aspnet-core/web-apis/background-services#an-external-job-queue).

## Implementation

<!-- TODO: Job creation, scheduling, monitoring -->

## Error Handling

<!-- TODO: Retries, dead letter -->

### Alerting on how long work has waited

- TODO: Alert when the oldest queued job is older than the wait you promised. Length is not that signal. See [Age of the oldest item](/devops/monitoring/alerting#age-of-the-oldest-item).

### One retry owner per job

- TODO: One layer owns the retries for a job. See [Retries at every layer](/fundamentals/distributed-systems/failure-and-degradation#retries-at-every-layer) and [Retry budget](/fundamentals/distributed-systems/failure-and-degradation#retry-budget).

## Reliable messaging

<!-- TODO: Publish domain events through an outbox -->

### How the outbox leaves the database

- TODO: Several workers can poll the outbox, or one process can read the database log. Order per aggregate and at-least-once delivery stay either way. See [Relaying: polling workers vs log-based](/patterns/integration-patterns/outbox-and-idempotent-consumer#relaying-polling-workers-vs-log-based).

### Indexing unsent messages

- TODO: Index the outbox rows that are still unsent, and leave the sent rows out of that index. See [Filtered indexes](/databases/relational/indexes-and-query-plans#filtered-indexes).

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

### A workflow as one method

- TODO: Write one of those waits as a single workflow method instead of a chain of jobs. See [Durable execution in .NET](/patterns/integration-patterns/durable-workflows#durable-execution-in-net).

## A context in a background worker

- TODO: A job has no HTTP request, so it has no request-scoped context.
- TODO: Open a scope for that job, use a context from the scope, and dispose the scope before the next job starts.

## Related Topics

- See [Failure and degradation](/fundamentals/distributed-systems/failure-and-degradation)
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
