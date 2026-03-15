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
- Travel along the shortest edge connecting current vertex to an unvisited vertex
- Repeat until you have visited all vertices

This produces very non optimal solutions

#### Lower Bound Algorithm
Obtain a lower bound on the weight of any Hamilton path:
1. Choose any vertex $v$. Delete it and all incident edges
2. Find a minimum weight spanning tree using [[Spanning Trees#Kruskal's Algorithm|Kruskal's]] or [[Spanning Trees#Prim's Algorithm|Prim's]] algorithm
3. Find the two edges incident with $v$ that have the smallest weight
4. The lower bound is the sum of the minimum weight spanning tree and the two edges