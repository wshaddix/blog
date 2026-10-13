---
title: Disposal
order: 30
---

# Disposal

The garbage collector frees memory. It does not close files, sockets, or database connections.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## IDisposable

What `Dispose` is for.

## using

A scope that always disposes, including when an exception is thrown.

## IAsyncDisposable

`await using` for resources whose cleanup is asynchronous.

## Ownership

Who creates a resource, and who is allowed to dispose it.

## Finalizers

Why a finalizer is the wrong tool for almost every class you write.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Memory and garbage collection](/fundamentals/programming-concepts/memory-and-gc)

---

**Next:** [Files, Streams, and JSON](/csharp/language-basics/files-streams-and-json)
