Find the shortest path between vertices $a$ and $f$ of a weighted graph

![[example_weighted_graph.png]]
$Vertices = \{a, b, c, d, e, f\}$
$Edges = \{(a, b, 3), (a, c, 2), (b, c, 3), (c, d, 4), (c, e, 6), (d, e, 5), (d, f, 1), (e, f, 6)\}$ (not directional)

*$D$ = the current shortest distance to every vertex (weight)*
*$E$ = is the vertex fully explored?*
$D = \{0, \infty, \infty, \infty, \infty, \infty\}$
$E = \{t, f, f, f, f, f\}$

$vertex = a$
*Update weights*
$D = \{0, 3, 2, \infty, \infty, \infty\}$
*Move to the lowest weight connected vertex that is unexplored*
$vertex = c$

*Repeat*
$vertex = c$
$D = \{0, 3, 2, 6, 8, \infty\}$
$E = \{t, t, t, f, f, f\}$

$v = d$
$D = \{0, 3, 2, 6, 8, 7\}$
$E = \{t, t, t, t, f, f\}$

$v = f$
$D = \{0, 3, 2, 6, 8, 7\}$
$E = \{t, t, t, t, f, t\}$

There is no connection with a lower weight, therefore $|a \rightarrow f| = 7$
The algorithm can keep going to find shortest paths to all vertices from $a$, but we terminate here
