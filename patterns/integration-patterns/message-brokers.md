---
title: Message Brokers
order: 85
---

# Message Brokers

A broker carries a message from a publisher to a consumer. A transport library is the client you put in front of the broker.

## Queues and topics

- TODO: A queue hands one message to one consumer. A topic hands a copy to each subscriber.
- TODO: Name the routing rule that decides which queue a published message lands in.

## What the library adds

- TODO: Retries, a saga, and an outbox are features of the library, not of the broker.
- TODO: The raw client publishes and consumes. Take a library when you would otherwise rebuild those features. The outbox on its own is [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer).

## When the license changes

- TODO: A library that becomes paid leaves three choices: pay, stay on the last release whose terms you accept, or replace it.
- TODO: Write down what each choice costs to keep running before you pick one.
- TODO: The same choice for an in-process dispatcher is [Mediator libraries and licensing](/patterns/application-patterns/cqrs#mediator-libraries-and-licensing).

## A dispatcher you write yourself

- TODO: A small in-process dispatcher is enough when there is one process and no broker.
- TODO: Replacing a bus means every retry, every saga, and every outbox path the library owned has to land somewhere else.

## Related Topics

- See [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)
- See [CQRS](/patterns/application-patterns/cqrs)
- See [Background services](/csharp/aspnet-core/web-apis/background-services)
- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview)

---

**Next:** [Outbox and the Idempotent Consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)
