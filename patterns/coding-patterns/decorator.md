# Decorator

A decorator wraps an object and adds behavior without changing the object's type. Middleware and HTTP handlers are decorators.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The shape

An interface, a wrapped implementation, and a class that implements the interface by calling the inner one.

## Middleware

A component that calls the next component.

## DelegatingHandler

A handler that calls the inner handler.

## Registration

The container builds the chain. You do not `new` the chain at the call site.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Middleware](/csharp/aspnet-core/middleware/overview)
- [HTTP clients](/csharp/platform/http-clients)

---

**Next:** [Coding Patterns](/patterns/coding-patterns/overview)
