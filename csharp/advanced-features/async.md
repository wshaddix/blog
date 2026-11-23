---
title: Async/Await
order: 50
---

# Async/Await

Write asynchronous code that reads like synchronous code.

## Why Async?

<!-- TODO: Responsiveness, scalability, I/O-bound vs CPU-bound -->

## Task and Task<T>

<!-- TODO: Representing async operations -->

## async and await Keywords

<!-- TODO: How they transform code, state machines -->

## Common Patterns

<!-- TODO: Async all the way, ConfigureAwait, cancellation -->

## Error Handling

<!-- TODO: Exceptions in async code, AggregateException -->

## Common Pitfalls

<!-- TODO: async void, blocking on async, deadlocks -->

## Cancellation

<!-- TODO: CancellationToken through the async call stack. See [Cancellation](/csharp/advanced-features/cancellation). -->

## Bounded concurrency

<!-- TODO: A cap on how much work runs at once -->

## Streaming results with IAsyncEnumerable

- TODO: Yield a row as it becomes ready instead of buffering the whole sequence first.
- TODO: Pass the caller's cancellation token into `await foreach` with `WithCancellation`.
- TODO: An endpoint can write that sequence as the response, one row at a time.
- TODO: A channel is the in-process queue for work of the same shape. See [Channels](/csharp/aspnet-core/web-apis/background-services#channels).
- TODO: An export that writes rows as they are read is [A streamed export](/building-a-saas/06-api-development/overview#a-streamed-export).

## ValueTask

- TODO: Return a `ValueTask` when the result is often already complete and a profile shows the `Task` allocation.
- TODO: Await a `ValueTask` once. A second await is not valid, and neither is reading the result after the await.
- TODO: Prefer `Task` on a path that is not hot. The simpler type is the default.

## Practical Examples

- See [Fundamentals: Concurrency](/fundamentals/programming-concepts/concurrency) - The theory
- See [ASP.NET Core Controllers](/csharp/aspnet-core/web-apis/overview) - Async in web apps

---

**Next:** [Cancellation](/csharp/advanced-features/cancellation)
