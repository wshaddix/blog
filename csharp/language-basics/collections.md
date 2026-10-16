---
title: Collections
order: 50
---

# Collections

Storing and organizing groups of objects.

## Arrays

<!-- TODO: Fixed-size, multidimensional, jagged -->

## List<T>

<!-- TODO: Dynamic arrays, common operations -->

## Dictionary<TKey, TValue>

<!-- TODO: Key-value storage, when to use -->

## HashSet<T>

<!-- TODO: Unique values, set operations -->

## Frozen collections

- TODO: Use `FrozenSet<T>` or `FrozenDictionary<TKey, TValue>` when the data is built once and then only read.
- TODO: Keep `HashSet<T>` while the set still changes. A `List<T>` membership test walks every item.
- TODO: Freeze after the last write. A later change means building another frozen collection.

## Queue<T> and Stack<T>

<!-- TODO: FIFO and LIFO structures -->

## Choosing the Right Collection

| Need | Collection |
|------|------------|
| Indexed access | List<T> or Array |
| Key-value lookup | Dictionary<TKey, TValue> |
| Unique values | HashSet<T> |
| Read-only lookup | FrozenSet<T> or FrozenDictionary |
| FIFO processing | Queue<T> |
| LIFO processing | Stack<T> |
| Sorted data | SortedList, SortedDictionary |

## Practical Examples

- See [Fundamentals: Data Structures](/fundamentals/data-structures/arrays) for the theory behind these collections
- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - Plan and tenant lookups on a hot path

---

**Next:** [Advanced Features](/csharp/advanced-features/generics)
