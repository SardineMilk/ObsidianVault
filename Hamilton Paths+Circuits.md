Let $G$ be a connected graph with vertices $V$ and edges $E$

A **hamilton circuit** is a simple circuit that visits every vertex of $G$ exactly once
A **hamilton path** is a simple path that visits every vertex of $G$ exactly once

It does not have to use all of the edges

There is no simple way to determine if a graph has a hamilton path/circuit or not

### Complete Graph
A complete graph has one edge between any (each) pair of vertices
A complete graph *always* contains a hamilton circuit

### Weighted Graphs
Finding Hamilton Circuit with minimum weight
This is the **travelling salesman problem**

#### Nearest Neightboor Algorithm
- Select a vertex as starting vertex
- Travel along an edge with the smallest weight to a vertex you have not been before
- Repeat until you have visited all vertices
This produces very non optimal solutions