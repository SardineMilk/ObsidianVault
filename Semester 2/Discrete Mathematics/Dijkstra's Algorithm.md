Find the shortest path between vertices $a$ and $f$ of a weighted graph
All weights must be non-negative

### Algorithm
##### At the start:
Create a "distances" array, one per vertex. 
Initially each value is infinity, or other large number
Set the element corresponding to the starting vertex to $0$
This stores the lowest found distance from the starting vertex to each vertex in the graph.
Also written as $L(v)$, the element corresponding to $v$ 

Create an "explored" array, one per vertex
Initially each value is false
Whenever you explore a vertex, set its element true so you know not to explore it again
If $v$ is explored, you know $L(v)$ is the smallest possible length 

If you want to find the vertices on the shortest path,
Keep another array that stores, for each vertex, the index of the vertex the shortest path was last updated by.
You can think of this like an arrow pointing backwards along the shortest path
To find the vertices of the shortest path, traverse backwards from the end vertex along these arrows

##### Loop until all vertices explored:
Choose the unexplored vertex with the lowest weight
Set its "explored" value to true

Update the distances array based on data from the new vertex
This will only affect adjacent vertices


### Example
![[example_weighted_graph.png]]
$Vertices = \{a, b, c, d, e, f\}$
$Edges = \{(a, b, 3), (a, c, 2), (b, c, 3), (c, d, 4), (c, e, 6), (d, e, 5), (d, f, 1), (e, f, 6)\}$ (not directional)
$starting\_vertex = a$

*$D$ = the current shortest distance to every vertex (weight)*
*$E$ = is the vertex fully explored?*
$D = \{0, \infty, \infty, \infty, \infty, \infty\}$
$E = \{t, f, f, f, f, f\}$

*Move to the lowest weight vertex that is unexplored*
$vertex = a$
*Update weights based on new vertex data*
$D = \{0, 3, 2, \infty, \infty, \infty\}$

*Repeat*
$vertex = c$
$D = \{0, 3, 2, 6, 8, \infty\}$
$E = \{t, f, t, f, f, f\}$

$vertex = b$
$D = \{0, 3, 2, 6, 8, \infty\}$
$E = \{t, t, t, f, f, f\}$

$v = d$
$D = \{0, 3, 2, 6, 8, 7\}$
$E = \{t, t, t, t, f, f\}$

$v = f$
$D = \{0, 3, 2, 6, 8, 7\}$
$E = \{t, t, t, t, f, t\}$

There is no connection with a lower weight, therefore $|a \rightarrow f| = 7$
The algorithm can keep going to find shortest paths to all vertices from $a$, but terminate here if you want a specific vertex

$v = e$
$D = \{0, 3, 2, 6, 8, 7\}$
$E = \{t, t, t, t, t, t\}$

This is the end of the full algorithm