# CQRS

Separate the model that changes state from the model that reads it, when those two models want different shapes.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## A command

A request that changes state and returns little.

## A query

A request that returns a shape the screen needs and changes nothing.

## When it pays

A write model and a read model that have diverged.

## When it does not

A CRUD screen where one model is still honest.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Repository](/patterns/application-patterns/repository)

---

**Next:** [Repository](/patterns/application-patterns/repository)
