# High-Performance C#

Primitives you reach for when an ordinary allocation shows up on a hot path.

## Performance primitives

## Lookups inside a loop

- TODO: Build the lookup before the loop. Do not scan for the same key on every iteration.
- TODO: A `List<T>` check inside the loop is a scan per item. A set or dictionary keeps the check small.
- TODO: When the lookup data is fixed for the process, freeze it once and reuse that instance.

## Practical Examples

- See [Memory and Garbage Collection](/fundamentals/programming-concepts/memory-and-gc)
- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - Repeated lookups of tenant and plan data

## Related Topics

- See [Modern C#](/csharp/advanced-features/modern-csharp)
- See [Entity Framework Performance](/csharp/entity-framework/performance)

---

**Continue to:** [Entity Framework](/csharp/entity-framework/getting-started)
