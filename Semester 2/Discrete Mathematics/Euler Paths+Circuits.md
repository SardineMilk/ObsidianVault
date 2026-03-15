Let $G$ be a connected graph with vertices $V$ and edges $E$

A **Euler Path** is a simple path that contains every edge of $G$ exactly once
A **Euler Circuit** is a simple circuit that contains every edge of $G$ exactly once

$G$ has an Euler Circuit if and only if **every vertex has an even degree** 
$G$ has an Euler Path if and only if **exactly two vertices have an odd degree** 

### Fleury's Algorithm
To construct an **Euler Circuit**:

Choose a starting vertex
Repeatedly add an incident edge (to the end of the last edge chosen)
Once you add an edge, remove it
Remove vertices of degree 0
Only use a *cut edge* if there's no alternative

(a cut edge would, when removed, make more connected components)
