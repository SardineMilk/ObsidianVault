Let $G$ be a connected graph
A **spanning tree** of $G$ is a subgraph of $G$ that contains every vertex of $G$ and is a tree

![[spanning-trees.png]]

A spanning tree uses the least possible number of edges to connect a graph

### Creating Spanning Trees
#### Breadth First
"visits all vertices adjacent to the current one before penetrating deep into a graph"

If a vertex is distance $i$ from vertex 1, it is in level $i$ of the spanning graph

##### Algorithm
Start at vertex 1
Iterate until all vertices added:
	Look at all adjacent vertices in numerical order
	If the new vertex does not form a simple circuit, add it to the tree
	These are level $i$ of the spanning tree
	Repeat for level $i+1$


#### Depth First
"penetrates as deeply as possible into a graph before fanning out to other vertices"

##### Algorithm
Start with vertex 1
Iterate until all vertices added
	Add vertex adjacent to vertices already in the tree, as long as it doesn't form a simple circuit
	If this isn't possible, backtrack until it is, then branch 


### Minimum Spanning Trees
Spanning tree of weighted graph $G$ with the smallest possible weight

You need to know two ways of finding MST's:
#### Kruskal's Algorithm
Step 1:
Put any edge with the smallest weight into the spanning tree $T$

Step 2:
Add any edge of minimum weight that does not form a simple circuit with $T$

Repeat until $n-1$ edges are in $T$


#### Prim's Algorithm
Step 1:
Put any edge with the smallest weight into the spanning tree $T$

Step 2:
Add any edge of minimum weight *adjacent to a vertex in $T$* that does not form a simple circuit with $T$

Repeat until $n-1$ edges are in $T$
