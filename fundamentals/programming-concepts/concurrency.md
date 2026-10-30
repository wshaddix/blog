---
title: Concurrency
order: 30
---

# Concurrency and Parallelism

Concurrency is managing multiple tasks that can be in progress at the same time. Parallelism is actually executing multiple tasks simultaneously.

## Concurrency vs Parallelism

| Aspect | Concurrency | Parallelism |
|--------|-------------|-------------|
| Definition | Dealing with many things at once | Doing many things at once |
| Goal | Structure | Speed |
| Hardware | Can work on 1 core | Requires multiple cores |
| Example | Handling multiple web requests | Processing array elements in parallel |

**Analogy:**
- **Concurrency:** One chef managing multiple dishes, switching between them
- **Parallelism:** Multiple chefs each cooking a different dish

## Why Concurrency Matters

- **Responsiveness:** UI doesn't freeze during long operations
- **Throughput:** Handle many requests simultaneously
- **Performance:** Utilize multiple CPU cores
- **Resource efficiency:** Don't waste time waiting for I/O

## Key Concepts

### Threads

The basic unit of execution. Multiple threads can run concurrently (or in parallel on multiple cores).

**Challenges:**
- Expensive to create/destroy
- Context switching overhead
- Shared memory requires synchronization

### Processes

Isolated execution environments with their own memory space.

**Comparison to threads:**
- More isolation (safer)
- Higher overhead
- Communication is explicit (IPC)

### Async/Await

Asynchronous programming model that doesn't block threads while waiting for I/O.

**Key insight:** async is about *not blocking*, not about parallelism.

### Thread Pool

A pool of reusable threads managed by the runtime. More efficient than creating threads manually.

## Common Problems

### Race Condition

Two threads access shared data, and the result depends on timing.

**Example:** Both threads read balance = 100, both subtract 50, final balance = 50 (should be 0)

### Deadlock

Two or more threads wait for each other indefinitely.

**Example:** Thread A holds lock X, waits for Y. Thread B holds Y, waits for X.

### Starvation

A thread never gets resources it needs because other threads keep taking them.

### Livelock

Threads keep responding to each other but make no progress (like two people in a hallway both stepping aside repeatedly).

### Starting too many at once

Awaiting every item at once can use up a shared resource before the work finishes.

- TODO: Contrast waiting on the whole set with a limit on how many items run together.
- TODO: Say which limit is reached first: connections from a pool, open sockets, or a rate limit on the service being called.
- TODO: Show three ways to set that limit: a `SemaphoreSlim`, `Parallel.ForEachAsync` with a maximum degree of parallelism, and a fixed set of workers reading from a channel.
- TODO: Explain how to pick the number for the workload in front of you.
- TODO: Describe what happens to the remaining work, including cancellation, when one task throws. See [Fan-out and the connection pool](/building-a-saas/07-data-layer/overview#fan-out-and-the-connection-pool).

## Synchronization Primitives

| Primitive | Use Case |
|-----------|----------|
| Lock/Mutex | Exclusive access to a resource |
| Semaphore | Limit concurrent access (N at a time) |
| ReaderWriterLock | Many readers OR one writer |
| Interlocked | Atomic operations on simple values |
| Monitor | Lock + wait/signal capability |
| Barrier | Synchronize multiple threads at a point |

### Lock granularity

- TODO: A lock that covers unrelated work makes every caller wait, even when they do not touch the same data.
- TODO: Give each key its own lock so an update to one key does not block an update to another.
- TODO: Finer locks have a cost. Take them in a fixed order when one operation needs several keys, or two callers can deadlock.
- TODO: In C#, compare one lock for the whole set with a `SemaphoreSlim` held per key.
- TODO: Measure throughput for both arrangements on the real workload before you keep the finer locks. See [Narrow locks](/building-a-saas/07-data-layer/overview#narrow-locks).

## Best Practices

1. **Prefer async/await over manual threading** for I/O-bound work
2. **Prefer immutable data** to avoid synchronization needs
3. **Keep critical sections small** - minimize time holding locks
4. **Avoid nested locks** to prevent deadlocks
5. **Use thread-safe collections** when sharing data
6. **Don't block async code** - avoid `.Result` and `.Wait()`

## Mental Models

- **Threads:** Workers in a warehouse
- **Locks:** A single bathroom key - only one person at a time
- **Semaphore:** Parking lot with limited spaces
- **Async:** Ordering food and doing something else while waiting

## CPU-Bound vs I/O-Bound

| Type | Example | Solution |
|------|---------|----------|
| CPU-bound | Image processing, calculations | Parallelism (Parallel.For, PLINQ) |
| I/O-bound | Database calls, HTTP requests | Async/await |

**Key rule:** Don't use parallelism for I/O-bound work; don't use async for CPU-bound work.

## Practical Examples in C#

- See [Async/Await](/csharp/advanced-features/async) - Asynchronous programming
- See [C# Collections](/csharp/language-basics/collections) - Including concurrent collections

## Practice Exercises

<!-- TODO: Add exercises -->

---

**Continue to:** [C# Language](/csharp/overview) - Apply these concepts in C#
