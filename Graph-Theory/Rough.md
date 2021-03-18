### Eulerian Graph

An Eulerian Graph is an undirected graph whose entire edge set can be
traversed starting at some vertex and returning to the same vertex,
without repeating any edge.

- Every vertex must have even degree
- There must be only 1 component with edges

Degree formula for decomposition of G into K edge disjoint subgraphs
G1,....,Gk.

### Degree Sequences and Graph Representation in a Computer

- Adjacency Matrix
- Adjacency List
- Incidence Matrix (Vertex x Edge)

# 2020-10-05

### Kernel of the Graph
**Kernel**: Contains just a single vertex, no edges.

**Strongly connected component**:A directed graph is
strongly connected if there is a path between all pairs of vertices.

Replace each strongly connected component with single vertex to get 
_kernel_.

**Tournament** is any orientation of a complete graph.

**Hamiltonian Paths** is a path that covers all the vertices.
It's a NP-Complete problem.

Every tournament has a Hamiltonian Path. It can be found by
simple greedy algorithm.

A tournament is either acyclic or has a triangle.

In a tournament, there is always a vertex reachable from every
other vertex in atmost two steps.

# 2020-10-07

### Trees
- A connected undirected acyclic graph.
- Connected graph on n-1 edges
- A tree on n vertices, always has n-1 edges

Drawing the edges of a tree starting with the vertex set
and no edges requires at least n-1 edge additions to
render it connected

Drawing an extra edge in an existing graph either
results in no change in the number of components or
decrease in number of components...

All trees are bipartite graph. A graph is bipartite if and only if
the graph has no odd cycles. A tree has no cycles and hence bipartite.

Leaf is a node of degree one in a tree. Other nodes are called
internal nodes.

The larger partite set always has a leaf. If the partite sets are of
equal size then both partite sets have leaves.

- An edge is a cut-edge if and only if, it lies on no cycle. Every
edge of a tree is a cut-edge.
- Every internal vertex of a tree is a cut-vertex.
- Every leaf is a non-cut-vertex.
- All maximal paths in a tree are leaf-to-leaf.
- Every pair of vertices have a unique path. (because there is no cycle)

[Lost Network...]

- Path is a special case of tree.
- Odd length maximal (Leaf-to-Leaf) path in a tree implies
a leaf in each partite set.

Every tree on at least two vertices, has at least two leaves.

Whenever you remove a leaf from a tree, you get a smaller tree.

So you can eliminate all the vertices of a tree by picking them in a
sequence of degree almost 1, in the residual sequence.

1-Degenerate === Forests
