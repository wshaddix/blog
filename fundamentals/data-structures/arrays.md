---
title: Arrays
order: 1
---

# Arrays

Arrays are the most fundamental data structure - a contiguous block of memory storing elements of the same type.

## Key Characteristics

| Property | Value |
|----------|-------|
| Access by index | O(1) |
| Search (unsorted) | O(n) |
| Search (sorted) | O(log n) with binary search |
| Insert at end | O(1) amortized |
| Insert at position | O(n) |
| Delete | O(n) |
| Memory | Contiguous, cache-friendly |

## When to Use Arrays

**Use arrays when:**
- You need fast random access by index
- The size is known or relatively stable
- You're iterating through elements sequentially
- Memory locality matters for performance

**Avoid arrays when:**
- Frequent insertions/deletions in the middle
- Size changes dramatically
- You need fast lookups by value (use a hash table)

## Mental Model

Think of an array like a row of numbered lockers. You can instantly go to locker #47 (random access), but if you need to insert a new locker between #23 and #24, everyone from #24 onward needs to move down.

## Common Operations

<!-- TODO: Add code examples -->

## Practical Examples in C#

- See [C# Collections](/csharp/language-basics/collections) for implementation details
- See [LINQ](/csharp/advanced-features/linq) for querying arrays

## Practice Problems

<!-- TODO: Add practice problems with solutions -->

---

**Next:** [Linked Lists](/fundamentals/data-structures/linked-lists) - When you need dynamic sizing
