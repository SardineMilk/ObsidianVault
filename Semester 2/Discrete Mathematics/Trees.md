A tree is a [[Connectivity|connected]] [[Graphs|graph]] that contains no simple circuits

Let $T$ be a graph on $n$ vertices
The following statements are equivalent:
- $T$ is a tree
- $T$ is connected and has $n-1$ edges
- Any two vertices in $T$ are connected by exactly one path
- $T$ is connected and removing any edge makes it disconnected

If any of these statements is true, then they all are true

A **forest** is a graph where every connected component is a tree
The **root** is the origin of the tree
**Leaves** are vertices of degree one, the ends of the graph. The root is not a leaf


### Properties
$V = I + L$
$E = V - 1$


### Full Trees
A tree is called a full m-ary tree (binary for m = 2, ternary for
m = 3) if each internal vertex except for the root has degree m + 1 and the root
vertex has degree m.

**Example:**
In a full binary tree:
- The root has degree 2
- Each internal vertex has degree 3

Property: In a full binary tree, 
$L = I+1$
$E = 2I$

A full $m$-ary tree has $m * I$ edges