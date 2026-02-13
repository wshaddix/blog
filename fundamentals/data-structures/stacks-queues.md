---
title: Stacks & Queues
order: 3
---

# Stacks and Queues

Stacks and queues are abstract data types (ADTs) that restrict how elements are added and removed, providing specific ordering guarantees.

## Stack (LIFO - Last In, First Out)

Think of a stack of plates - you can only add or remove from the top.

### Key Operations

| Operation | Description | Time Complexity |
|-----------|-------------|-----------------|
| Push | Add to top | O(1) |
| Pop | Remove from top | O(1) |
| Peek | View top without removing | O(1) |
| IsEmpty | Check if empty | O(1) |

### Common Use Cases

- **Undo functionality** - Each action pushed, undo pops
- **Expression evaluation** - Parsing mathematical expressions
- **Call stack** - Function calls and returns
- **Backtracking algorithms** - DFS, maze solving
- **Browser history** - Back button behavior

## Queue (FIFO - First In, First Out)

Think of a line at a store - first person in line is first served.

### Key Operations

| Operation | Description | Time Complexity |
|-----------|-------------|-----------------|
| Enqueue | Add to back | O(1) |
| Dequeue | Remove from front | O(1) |
| Peek | View front without removing | O(1) |
| IsEmpty | Check if empty | O(1) |

### Common Use Cases

- **Task scheduling** - Process jobs in order received
- **BFS traversal** - Level-order tree/graph traversal
- **Message queues** - Async communication between services
- **Print spooling** - Documents printed in order submitted
- **Request handling** - Web server request queues

## Variants

| Variant | Description |
|---------|-------------|
| Deque (Double-ended queue) | Add/remove from both ends |
| Priority Queue | Elements dequeued by priority, not order |
| Circular Queue | Fixed-size queue that wraps around |

## Mental Model

- **Stack**: A Pringles can - you can only access the top chip
- **Queue**: A tunnel - cars exit in the same order they entered

## Common Operations

<!-- TODO: Add code examples -->

## Practical Examples in C#

- See [C# Collections](/csharp/language-basics/collections) for Stack<T> and Queue<T> implementations

## Practice Problems

<!-- TODO: Add practice problems with solutions -->

---

**Next:** [Hash Tables](/fundamentals/data-structures/hash-tables) - O(1) lookups by key
