---
title: Linked Lists
order: 2
---

# Linked Lists

A linked list is a sequence of nodes where each node contains data and a reference (pointer) to the next node.

## Types of Linked Lists

| Type | Description | Use Case |
|------|-------------|----------|
| Singly Linked | Each node points to next | Simple forward traversal |
| Doubly Linked | Nodes point to next and previous | Bidirectional traversal |
| Circular | Last node points to first | Round-robin scheduling |

## Key Characteristics

| Property | Singly Linked | Doubly Linked |
|----------|---------------|---------------|
| Access by index | O(n) | O(n) |
| Insert at head | O(1) | O(1) |
| Insert at tail | O(n) or O(1)* | O(1) |
| Insert at position | O(n) | O(n) |
| Delete at head | O(1) | O(1) |
| Delete at position | O(n) | O(n) |
| Memory overhead | 1 pointer per node | 2 pointers per node |

*O(1) if you maintain a tail pointer

## When to Use Linked Lists

**Use linked lists when:**
- Frequent insertions/deletions at the beginning
- You don't know the size upfront
- You don't need random access
- Implementing stacks, queues, or other ADTs

**Avoid linked lists when:**
- You need random access by index
- Memory is constrained (pointer overhead)
- Cache performance matters (non-contiguous memory)

## Mental Model

Think of a linked list like a scavenger hunt. Each clue (node) tells you where to find the next clue. You can't jump directly to clue #5 - you have to follow the chain from the beginning.

## Common Operations

<!-- TODO: Add code examples -->

## Practical Examples in C#

- See [C# Collections](/csharp/language-basics/collections) for the built-in LinkedList<T> implementation

## Practice Problems

<!-- TODO: Add practice problems with solutions -->

---

**Next:** [Stacks & Queues](/fundamentals/data-structures/stacks-queues) - Specialized linear structures
