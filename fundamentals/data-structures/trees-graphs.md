---
title: Trees & Graphs
order: 5
---

# Trees and Graphs

Trees and graphs represent hierarchical and networked relationships between data.

## Trees

A tree is a connected, acyclic graph with a designated root node.

### Key Terminology

| Term | Definition |
|------|------------|
| Root | The top node (no parent) |
| Parent | Node directly above |
| Child | Node directly below |
| Leaf | Node with no children |
| Height | Longest path from root to leaf |
| Depth | Distance from root to a node |
| Subtree | A node and all its descendants |

### Common Tree Types

| Type | Description | Use Case |
|------|-------------|----------|
| Binary Tree | Each node has at most 2 children | Expression parsing, decisions |
| Binary Search Tree (BST) | Left < parent < right | Sorted data, searching |
| AVL Tree | Self-balancing BST | When balance is critical |
| Red-Black Tree | Self-balancing BST | .NET SortedDictionary |
| B-Tree | Multi-way tree, balanced | Databases, file systems |
| Trie | Prefix tree | Autocomplete, spell check |
| Heap | Complete tree with heap property | Priority queues |

### BST Operations

| Operation | Average | Worst (unbalanced) |
|-----------|---------|-------------------|
| Search | O(log n) | O(n) |
| Insert | O(log n) | O(n) |
| Delete | O(log n) | O(n) |

## Graphs

A graph is a set of vertices (nodes) connected by edges.

### Graph Types

| Type | Description |
|------|-------------|
| Directed | Edges have direction (A → B) |
| Undirected | Edges are bidirectional |
| Weighted | Edges have values (distances, costs) |
| Cyclic | Contains at least one cycle |
| Acyclic | No cycles (DAG if directed) |

### Graph Representations

| Representation | Space | Edge Check | Iterate Neighbors |
|----------------|-------|------------|-------------------|
| Adjacency Matrix | O(V²) | O(1) | O(V) |
| Adjacency List | O(V+E) | O(degree) | O(degree) |

### Common Graph Algorithms

| Algorithm | Purpose | Time Complexity |
|-----------|---------|-----------------|
| BFS | Shortest path (unweighted) | O(V+E) |
| DFS | Traversal, cycle detection | O(V+E) |
| Dijkstra | Shortest path (weighted, non-negative) | O((V+E) log V) |
| Bellman-Ford | Shortest path (negative weights) | O(VE) |
| Topological Sort | Order DAG nodes | O(V+E) |

## When to Use What

**Use trees when:**
- Data has natural hierarchy (org chart, file system)
- You need sorted data with fast operations (BST)
- Implementing priority queues (heap)

**Use graphs when:**
- Modeling networks (social, road, computer)
- Dependencies between items (build systems)
- Any relationship that isn't strictly hierarchical

## Mental Models

- **Tree**: A family tree - one ancestor at the top, branches downward
- **Graph**: A map of cities connected by roads - any city can connect to any other

## Practical Examples in C#

- See [C# Collections](/csharp/language-basics/collections) for SortedDictionary, SortedSet, and PriorityQueue<T>

## Practice Problems

<!-- TODO: Add practice problems with solutions -->

---

**Continue to:** [Algorithms](/fundamentals/algorithms/big-o-notation) - Learn how to work with these structures efficiently
