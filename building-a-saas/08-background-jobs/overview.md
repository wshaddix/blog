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

## Job Processing Options

| Option | Pros | Cons |
|--------|------|------|
| Hosted Service | Simple, in-process | Tied to web app lifecycle |
| Hangfire | Full-featured, dashboard | Additional complexity |
| Azure Functions | Serverless, scalable | Cold starts, deployment |

## Implementation

## Error Handling

## Reliable messaging

## Shutdown and cancellation

## When a saga needs a person

## Related Topics

- See [Azure Functions](/devops/azure/functions)
- See [Fundamentals: Concurrency](/fundamentals/programming-concepts/concurrency)
- See [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)
- See [Background services](/csharp/aspnet-core/web-apis/background-services)
- See [Sagas](/patterns/integration-patterns/sagas)

---

**Next:** [Chapter 9: Billing Integration](/building-a-saas/09-billing-integration/overview)
