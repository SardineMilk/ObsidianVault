An *adjacency matrix* is a square matrix 
The side length is equal to the number of nodes in the graph
$a_{ij}$ = How many connections node $i$ has to node $j$

In a simple graph:
- Every element on the diagonal is 0 
	- No node is adjacent to itself
- Every element is either 0 or 1
	- No element has multiple connections to another

In a non-directed graph:
- The adjacency matrix is symmetrical on the diagonal
	- $a_{ij} = a_{ji}$

**Example:**
![[example_graph.png]]
Fig 1
$V = \{a, b, c, d\}$
$E = \{(a, b), (a, d), (b, d), (c, d)\}$

$A =$
0 1 0 1
1 0 0 1
0 0 0 1
1 1 1 0

To find the number of connections from $b$ to $d$:
- Indices: $b = 2$, $d = 4$
- $A_{2,4} = 1$
- There is one connection from $b$ to $d$


### Paths of length $n$
To find the number of paths of length $n$ from $i$ to $j$:
- Raise $A$ to the power of $n$
- $(A^n)_{i, j}$ is the number of paths

To raise $A^n$, [[Matrices#Multiplication| multiply]] $A$ by itself $n$ times

$A =$
0 1 0 1
1 0 0 1
0 0 0 1
1 1 1 0

$A * A =$
2 1 1 1
1 2 1 1 
1 1 1 0
1 1 0 3
*The diagonal is the connectivity of each node - to each neighbour and back*