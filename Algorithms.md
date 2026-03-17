"edges incident to $v$" mean any edges where $v$ is one of the two vertices 
"vertices adjacent to $v$" mean any vertices connected to $v$ by at least one edge. 
vertices $u$ and $v$ are adjacent if there exists at least one edge incident to both $u$ and $v$ 

### Weighted Graphs
#### Dijkstra's 
Find the minimum weight path from $a$ to any other vertex on weighted graph $G$

Create a "distances" array, one per vertex. 
Initially each value is infinity, or other large number
Set the element corresponding to the starting vertex to $0$

Create an "explored" array, initially empty
##### Loop until all vertices explored
Choose the unexplored vertex with the lowest weight
Add it to the explored array

Update the distances array based on data from the new vertex
This will only affect adjacent vertices


### Spanning Trees
Create a spanning tree from graph $G$ 

#### Breadth First
Start at vertex 1
Iterate until all vertices added
	Look at all adjacent vertices in numerical order
	If the new vertex does not form a simple circuit, add it to the tree
	These are level $i$ of the spanning tree
	Repeat for level $i+1$

#### Depth First
Start with vertex 1
Iterate until all vertices added
	Add adjacent vertices in numerical order, as long as it doesn't form a simple circuit
	Continue extending the tree from the most recently added vertex whenever possible.
	If this isn't possible, backtrack until it is, then branch 


### Minimum Spanning Trees
Find the minimum spanning tree of weighted graph $G$
#### Kruskal's Algorithm
Put the edge with the smallest weight into the spanning tree $T$
Repeat until $n-1$ edges are in $T$
	Add any edge of minimum weight that does not form a simple circuit with $T$

#### Prim's Algorithm
Put the edge with the smallest weight into the spanning tree $T$
Repeat until $n-1$ edges are in $T$
	Add any edge of minimum weight *incident to a vertex in $T$* that does not form a simple circuit with $T$


### Euler Circuits/Paths
A simple circuit/path that uses every edge of $G$ exactly once

Construct an Euler Circuit from graph $G$
#### Fleury's Algorithm
Choose any starting vertex
Repeat until all edges added
	Add an edge incident to the end of the last edge chosen
	Only choose a *cut edge* if there's no alternative
	Once you add an edge, remove it from the graph
	Remove vertices of degree 0 from the graph


### Hamilton Circuits/Paths
A simple circuit/path that visits every vertex in $G$ exactly once

Construct a Hamilton Circuit from graph $G$
#### Nearest Neighboor Algorithm
Select the starting vertex
Repeat until all vertices visited
	Travel along the incident edge with the smallest weight 
	Only travel along an edge if the adjacent vertex has not been visited yet


Find a lower bound for the weight of any Hamilton Path
#### Lower Bound Algorithm
Choose any vertex $v$ and remove it along with all incident edges from $G$
Use *Prim's* or *Kruskal's* algorithm to find the minimum weight spanning tree in the new graph
Find the two edges incident with $v$ that have the smallest weight
Sum the weights of the minimum spanning tree and the two edges 