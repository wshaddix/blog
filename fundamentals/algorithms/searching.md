---
title: Searching Algorithms
order: 3
---

# Searching Algorithms

Searching is finding an element in a data structure. The right algorithm depends on the structure and whether data is sorted.

## Comparison of Searching Algorithms

| Algorithm | Data Structure | Sorted? | Time | Space |
|-----------|---------------|---------|------|-------|
| Linear Search | Array/List | No | O(n) | O(1) |
| Binary Search | Array | Yes | O(log n) | O(1) |
| Hash Lookup | Hash Table | N/A | O(1) avg | O(n) |
| BST Search | Binary Search Tree | N/A | O(log n) avg | O(n) |
| BFS | Graph | N/A | O(V+E) | O(V) |
| DFS | Graph | N/A | O(V+E) | O(V) |

## Linear Search

The simplest approach - check each element one by one.

**When to use:**
- Unsorted data
- Small datasets
- You only search once (not worth sorting)
- Linked lists (binary search doesn't help)

## Binary Search

Repeatedly divide the search space in half.

**Requirements:**
- Data must be sorted
- Random access (arrays, not linked lists)

**Key insight:** Each comparison eliminates half the remaining elements.

### Binary Search Variants

| Variant | Purpose |
|---------|---------|
| Standard | Find exact match |
| Lower Bound | First element >= target |
| Upper Bound | First element > target |
| Rotated Array | Search in rotated sorted array |

### Common Pitfalls

1. **Off-by-one errors** - Boundary conditions are tricky
2. **Integer overflow** - `(low + high) / 2` can overflow; use `low + (high - low) / 2`
3. **Infinite loops** - Wrong update to low/high

## Graph Traversals

### BFS (Breadth-First Search)

Explores neighbors level by level using a queue.

**Use for:**
- Shortest path in unweighted graphs
- Level-order tree traversal
- Finding all nodes within k steps

### DFS (Depth-First Search)

Explores as far as possible before backtracking using recursion/stack.

**Use for:**
- Detecting cycles
- Topological sorting
- Pathfinding (when any path works)
- Maze solving

### BFS vs DFS

| Aspect | BFS | DFS |
|--------|-----|-----|
| Data structure | Queue | Stack/Recursion |
| Memory | O(branching factor × depth) | O(depth) |
| Finds shortest path | Yes (unweighted) | No |
| Explores | Level by level | Branch by branch |

## Mental Models

- **Linear Search**: Reading a book page by page to find a word
- **Binary Search**: Looking up a word in a dictionary - open to the middle, go left or right
- **BFS**: Ripples spreading from a stone dropped in water
- **DFS**: Exploring a maze by following one path until you hit a dead end

## When to Use What

| Scenario | Algorithm |
|----------|-----------|
| Unsorted array, one-time search | Linear Search |
| Sorted array, many searches | Binary Search |
| Key-value lookups | Hash Table |
| Need ordering + search | BST / SortedDictionary |
| Shortest path (unweighted) | BFS |
| Detect cycles / explore all paths | DFS |

## Practical Examples in C#

- See [C# Collections](/csharp/language-basics/collections) for Array.BinarySearch and Dictionary lookups
- See [LINQ](/csharp/advanced-features/linq) for Contains, First, Single, and other search methods

## Practice Problems

<!-- TODO: Add practice problems -->

---

**Next:** [Recursion](/fundamentals/algorithms/recursion) - Solving problems by breaking them down
