---
title: Hash Tables
order: 4
---

# Hash Tables

A hash table (hash map, dictionary) stores key-value pairs with average O(1) lookup, insert, and delete operations.

## How It Works

1. **Hash Function**: Converts a key into an array index
2. **Buckets**: Array positions where values are stored
3. **Collision Handling**: Strategy when two keys hash to the same index

## Key Characteristics

| Operation | Average | Worst Case |
|-----------|---------|------------|
| Lookup | O(1) | O(n) |
| Insert | O(1) | O(n) |
| Delete | O(1) | O(n) |
| Space | O(n) | O(n) |

*Worst case occurs with many collisions (poor hash function or adversarial input)*

## Collision Resolution Strategies

| Strategy | Description | Pros | Cons |
|----------|-------------|------|------|
| Chaining | Each bucket holds a linked list | Simple, handles many collisions | Extra memory for pointers |
| Open Addressing | Find next empty slot | Better cache performance | Clustering issues |
| Robin Hood Hashing | Steal from rich, give to poor | More even probe lengths | Complex implementation |

## When to Use Hash Tables

**Use hash tables when:**
- You need fast lookups by key
- Keys are unique (or you want to enforce uniqueness)
- Counting occurrences of items
- Caching/memoization
- Implementing sets

**Avoid hash tables when:**
- You need ordered data (use a tree)
- Keys are not hashable
- Memory is very constrained
- You need range queries

## Mental Model

Think of a hash table like a coat check. You give them your coat (value) and get a ticket number (hash of the key). Later, you show the ticket and instantly get your coat back - no searching through all the coats.

## Hash Function Properties

A good hash function should:
- Be **deterministic** - same input always produces same output
- Be **fast** to compute
- **Distribute uniformly** across the array
- **Minimize collisions** for expected input

## Common Operations

<!-- TODO: Add code examples -->

## Practical Examples in C#

- See [C# Collections](/csharp/language-basics/collections) for Dictionary<TKey, TValue> and HashSet<T>

## Practice Problems

<!-- TODO: Add practice problems with solutions -->

---

**Next:** [Trees & Graphs](/fundamentals/data-structures/trees-graphs) - Hierarchical and networked data
