---
title: Sorting Algorithms
order: 2
---

# Sorting Algorithms

Sorting is arranging items in a specific order. Understanding sorting algorithms teaches you algorithmic thinking and complexity trade-offs.

## Comparison of Sorting Algorithms

| Algorithm | Best | Average | Worst | Space | Stable? | Use Case |
|-----------|------|---------|-------|-------|---------|----------|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | Yes | Teaching only |
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) | No | Small datasets |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | Yes | Nearly sorted data |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes | Guaranteed performance |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | No | General purpose |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) | No | Memory constrained |
| Counting Sort | O(n+k) | O(n+k) | O(n+k) | O(k) | Yes | Small integer range |
| Radix Sort | O(nk) | O(nk) | O(nk) | O(n+k) | Yes | Fixed-length integers |

*Stable = maintains relative order of equal elements*

## When to Use What

### Quick Sort (Default Choice)
- General-purpose sorting
- When average-case performance matters
- Memory is limited

### Merge Sort
- When stability is required
- Sorting linked lists
- External sorting (data doesn't fit in memory)

### Insertion Sort
- Small datasets (< 50 elements)
- Nearly sorted data
- Online sorting (data arrives over time)

### Counting/Radix Sort
- Integer keys with limited range
- When O(n log n) isn't fast enough

## Key Concepts

### Stability
A stable sort maintains the relative order of items with equal keys.

Example: Sorting by last name, then by first name (stable sort keeps first name order within same last name)

### In-Place
An in-place sort uses O(1) extra space (not counting the input).

### Divide and Conquer
Merge sort and quick sort use this pattern:
1. Divide the problem into subproblems
2. Solve subproblems recursively
3. Combine solutions

## Algorithm Deep Dives

### Quick Sort
- Pick a "pivot" element
- Partition: elements < pivot go left, > pivot go right
- Recursively sort left and right

*Pitfall*: Poor pivot choice (first/last element) gives O(n²) on sorted input

### Merge Sort
- Split array in half
- Recursively sort each half
- Merge sorted halves

*Trade-off*: Guaranteed O(n log n) but needs O(n) extra space

## Mental Models

- **Bubble Sort**: Bubbles rising in water - largest elements "bubble up" to the end
- **Insertion Sort**: Sorting playing cards - pick up each card and insert it in the right place
- **Merge Sort**: Sorting a deck by splitting it, sorting each pile, then merging
- **Quick Sort**: Organizing books by picking one and putting smaller ones left, larger ones right

## Practical Examples in C#

- See [C# Collections](/csharp/language-basics/collections) for Array.Sort and List.Sort
- See [LINQ](/csharp/advanced-features/linq) for OrderBy and sorting operations

## Practice Problems

<!-- TODO: Add practice problems -->

---

**Next:** [Searching](/fundamentals/algorithms/searching) - Finding elements efficiently
