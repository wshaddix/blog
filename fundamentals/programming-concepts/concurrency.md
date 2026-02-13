---
title: Concurrency
order: 3
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

## Synchronization Primitives

| Primitive | Use Case |
|-----------|----------|
| Lock/Mutex | Exclusive access to a resource |
| Semaphore | Limit concurrent access (N at a time) |
| ReaderWriterLock | Many readers OR one writer |
| Interlocked | Atomic operations on simple values |
| Monitor | Lock + wait/signal capability |
| Barrier | Synchronize multiple threads at a point |

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
