---
title: Functional Concepts
order: 2
---

# Functional Programming Concepts

Functional programming (FP) treats computation as the evaluation of mathematical functions, emphasizing immutability and avoiding side effects.

## Why Learn Functional Concepts?

Even if you write primarily OOP code, functional concepts help you:
- Write more predictable, testable code
- Use LINQ effectively in C#
- Leverage async/parallel programming safely
- Understand modern language features

## Core Principles

### 1. Pure Functions

A pure function:
- Always returns the same output for the same input
- Has no side effects (doesn't modify external state)

**Why it matters:** Pure functions are predictable, testable, and cacheable.

```
// Pure - no side effects, deterministic
int Add(int a, int b) => a + b;

// Impure - depends on/modifies external state
int counter = 0;
int IncrementAndGet() => ++counter;
```

### 2. Immutability

Data structures are never modified after creation. Instead, create new versions with changes.

**Why it matters:**
- No shared mutable state = no race conditions
- Easier to reason about code
- Enables safe parallelism

### 3. First-Class Functions

Functions can be:
- Assigned to variables
- Passed as arguments
- Returned from other functions

This enables higher-order functions and composition.

### 4. Declarative Style

Describe *what* you want, not *how* to get it.

```
// Imperative (how)
var results = new List<int>();
foreach (var n in numbers)
    if (n > 5)
        results.Add(n * 2);

// Declarative (what)
var results = numbers.Where(n => n > 5).Select(n => n * 2);
```

## Key Concepts

### Higher-Order Functions

Functions that take functions as arguments or return functions.

Common examples:
- `Map` (Select) - Transform each element
- `Filter` (Where) - Keep elements matching predicate
- `Reduce` (Aggregate) - Combine elements into single value

### Function Composition

Building complex functions from simpler ones.

```
var processUser = Compose(Validate, Normalize, Save);
```

### Closures

Functions that capture variables from their enclosing scope.

```csharp
int multiplier = 3;
Func<int, int> multiply = x => x * multiplier;  // Captures 'multiplier'
```

### Currying and Partial Application

- **Currying:** Transforming a function with multiple arguments into a sequence of single-argument functions
- **Partial Application:** Fixing some arguments of a function, producing a function with fewer arguments

### Pattern Matching

Checking a value against patterns and destructuring it.

```csharp
string Describe(object obj) => obj switch
{
    int n when n > 0 => "positive integer",
    string s => $"string of length {s.Length}",
    null => "nothing",
    _ => "something else"
};
```

## Functional vs OOP

| Aspect | Functional | OOP |
|--------|------------|-----|
| Primary unit | Function | Object |
| State | Immutable | Mutable |
| Side effects | Avoided | Common |
| Data flow | Explicit (parameters) | Implicit (object state) |
| Polymorphism | Via functions | Via inheritance/interfaces |

**They're not mutually exclusive.** C# supports both, and modern code often blends them.

## When to Use Functional Style

**Good fit:**
- Data transformations (LINQ pipelines)
- Stateless computations
- Parallel/concurrent code
- Event processing

**Less ideal:**
- Heavy I/O operations
- Complex object interactions
- When mutability is more natural

## Practical Examples in C#

- See [LINQ](/csharp/advanced-features/linq) - Functional programming in C#
- See [Records](/csharp/advanced-features/records) - Immutable data types
- See [Pattern Matching](/csharp/advanced-features/pattern-matching) - Declarative conditionals

## Practice Exercises

<!-- TODO: Add exercises -->

---

**Next:** [Concurrency](/fundamentals/programming-concepts/concurrency) - Parallel and async programming
