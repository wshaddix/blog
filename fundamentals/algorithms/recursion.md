---
title: Recursion
order: 4
---

# Recursion

Recursion is a technique where a function calls itself to solve a smaller instance of the same problem.

## The Two Requirements

Every recursive solution needs:

1. **Base Case** - A condition that stops the recursion
2. **Recursive Case** - The function calls itself with a smaller/simpler input

Without a base case, you get infinite recursion (stack overflow).

## Anatomy of a Recursive Function

```
function solve(problem):
    if problem is simple enough:    // Base case
        return simple solution
    else:                           // Recursive case
        smaller = make problem smaller
        result = solve(smaller)     // Recursive call
        return combine(result)
```

## Classic Examples

| Problem | Base Case | Recursive Case |
|---------|-----------|----------------|
| Factorial n! | n = 0 → return 1 | n × factorial(n-1) |
| Fibonacci | n ≤ 1 → return n | fib(n-1) + fib(n-2) |
| Sum of array | empty → return 0 | first + sum(rest) |
| Tree traversal | null node → return | visit(node), recurse(children) |
| Binary search | found or empty | search(half) |

## Recursion vs Iteration

| Aspect | Recursion | Iteration |
|--------|-----------|-----------|
| Readability | Often cleaner for tree/graph problems | Usually clearer for linear problems |
| Space | O(n) stack space for n calls | O(1) typically |
| Performance | Function call overhead | Usually faster |
| Risk | Stack overflow | Infinite loops |

**Rule of thumb:** If the problem has a recursive structure (trees, graphs, divide-and-conquer), recursion is natural. Otherwise, prefer iteration.

## Tail Recursion

A recursive call is "tail recursive" if it's the last operation in the function. Some compilers optimize this to avoid stack growth.

```
// NOT tail recursive - multiplication happens after the call
factorial(n):
    if n == 0: return 1
    return n * factorial(n-1)

// Tail recursive - call is the last operation
factorial(n, accumulator=1):
    if n == 0: return accumulator
    return factorial(n-1, n * accumulator)
```

*Note: C# does not guarantee tail call optimization.*

## Common Patterns

### Divide and Conquer
1. Divide problem into subproblems
2. Solve subproblems recursively
3. Combine solutions

Examples: Merge sort, quick sort, binary search

### Backtracking
1. Make a choice
2. Recurse
3. If it doesn't work, undo the choice and try another

Examples: N-Queens, Sudoku solver, maze solving

### Dynamic Programming (Memoization)
Recursion + caching to avoid redundant calculations.

Example: Naive Fibonacci is O(2ⁿ), memoized is O(n)

## Debugging Recursion

1. **Trace by hand** - Write out the call stack for small inputs
2. **Check base case** - Does it actually stop?
3. **Check progress** - Does each call get closer to the base case?
4. **Print statements** - Log entry/exit with parameters

## Mental Model

Recursion is like looking up a word in a dictionary and finding it defined using another word. You keep looking up words until you find one you already know (the base case).

## Common Pitfalls

1. **Missing base case** - Infinite recursion
2. **Base case never reached** - Problem doesn't get smaller
3. **Too many recursive calls** - Stack overflow
4. **Redundant computation** - Exponential time (use memoization)

## Practical Examples in C#

- See [LINQ](/csharp/advanced-features/linq) for SelectMany and recursive operations
- See [Async/Await](/csharp/advanced-features/async) for async recursion patterns

## Practice Problems

<!-- TODO: Add practice problems -->

---

**Continue to:** [Programming Concepts](/fundamentals/programming-concepts/oop-principles) - OOP, functional programming, and more
