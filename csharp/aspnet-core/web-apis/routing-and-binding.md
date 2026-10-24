---
title: Routing and Model Binding
order: 180
---

# Routing and Model Binding

How a request URL and body become arguments on a handler.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Routes

Literals, parameters, and constraints.

## Binding sources

Route, query, header, and body.

## Records and request types

A request type per command, and why a domain entity is not a request body.

## Missing and extra fields

What the binder does with a field the client omitted.

## Large request bodies

- TODO: A bound body is read whole before the handler runs. A large JSON array costs that much memory per request.
- TODO: Read the body as a stream, and deserialize the items one at a time from the request's pipe.
- TODO: Set a size limit for the endpoint, and return 413 when a body is larger.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Validation](/csharp/aspnet-core/web-apis/validation)

---

**Next:** [Validation](/csharp/aspnet-core/web-apis/validation)
