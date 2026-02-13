---
title: Big O Notation
order: 1
---

# Big O Notation

Big O notation describes how an algorithm's time or space requirements grow as input size increases. It's the language engineers use to discuss performance.

## Why Big O Matters

Understanding Big O helps you:
- **Choose the right algorithm** for your problem size
- **Predict performance** before writing code
- **Identify bottlenecks** in existing code
- **Communicate** with other engineers about performance

## Common Complexities (Best to Worst)

| Big O | Name | Example | 10 items | 100 items | 1000 items |
|-------|------|---------|----------|-----------|------------|
| O(1) | Constant | Array index access | 1 | 1 | 1 |
| O(log n) | Logarithmic | Binary search | 3 | 7 | 10 |
| O(n) | Linear | Linear search | 10 | 100 | 1,000 |
| O(n log n) | Linearithmic | Merge sort | 33 | 664 | 9,966 |
| O(n²) | Quadratic | Bubble sort | 100 | 10,000 | 1,000,000 |
| O(2ⁿ) | Exponential | Recursive Fibonacci | 1,024 | 10³⁰ | 10³⁰¹ |
| O(n!) | Factorial | Traveling salesman (brute) | 3.6M | 10¹⁵⁸ | ... |

## Reading Big O

- **O(1)**: "Constant time" - doesn't depend on input size
- **O(n)**: "Linear time" - doubles when input doubles
- **O(n²)**: "Quadratic time" - 4x when input doubles

## Rules for Calculating Big O

### 1. Drop Constants
O(2n) → O(n)
O(500) → O(1)

### 2. Drop Lower-Order Terms
O(n² + n) → O(n²)
O(n + log n) → O(n)

### 3. Different Inputs = Different Variables
```
function(arrayA, arrayB):
    for each a in arrayA:      // O(a)
        for each b in arrayB:  // O(b)
            print(a, b)
// Total: O(a × b), NOT O(n²)
```

### 4. Add vs Multiply
- **Sequential** operations: ADD → O(A + B)
- **Nested** operations: MULTIPLY → O(A × B)

## Space Complexity

Big O also describes memory usage:

| Pattern | Space Complexity |
|---------|------------------|
| Fixed variables | O(1) |
| Array of size n | O(n) |
| 2D matrix n×n | O(n²) |
| Recursive call stack depth n | O(n) |

## Common Pitfalls

1. **Ignoring hidden loops** - String concatenation in a loop is O(n²)
2. **Forgetting space** - Recursive solutions use stack space
3. **Assuming constant time** - Hash table operations can degrade to O(n)
4. **Over-optimizing** - O(n²) might be fine for small n

## Mental Model

Big O is like asking "how does this scale?" not "how fast is this?"

- **O(1)**: Elevating a building 1 floor - same effort regardless of building size
- **O(n)**: Climbing stairs - twice the floors, twice the time
- **O(n²)**: Handshakes at a party - double the people, quadruple the handshakes

## Practical Examples in C#

- See [LINQ Performance Considerations](/csharp/advanced-features/linq) for common pitfalls
- See [Collection Performance](/csharp/language-basics/collections) for choosing the right collection

## Practice Problems

<!-- TODO: Add practice problems -->

---

**Next:** [Sorting](/fundamentals/algorithms/sorting) - Applying Big O analysis to sorting algorithms
