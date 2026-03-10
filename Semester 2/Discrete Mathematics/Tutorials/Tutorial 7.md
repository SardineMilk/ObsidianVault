1.
a) Weakly connected
b) Strongly connected

2.
a) (a, b, e), (c), (d)
b) (a), (b), (f), (c, d, e)

3.
A = 
0 1 1
1 0 0
0 2 0

A^2 =
1 2 0
0 1 1
2 0 0

A^3 = 
2 1 1 
1 2 0
0 2 2

A^4 = 
1 4 2
2 1 1
2 4 0

a) c->b length 4: 4 paths
b) a->b length 3: 1 path

4.
$V = \{a, b, c, d, e\}$
$E = \{(a, b, 4), (a, d, 2), (b, c, 3), (b, e, 3), (c, z, 2), (d, e, 3), (e, z, 1)\}$
Path from $a$ -> $z$

*Initial Arrays*
$D = \{0, \infty, \infty, \infty, \infty, \infty\}$
$E = \{\}$

$v = a$
$D = \{0, 4, \infty, 2, \infty, \infty\}$
$E = \{a\}$

$v = d$
$D = \{0, 4, \infty, 2, 5, \infty\}$
$E = \{a, d\}$

$v = b$
$D = \{0, 4, 7, 2, 5, \infty\}$
$E = \{a, b, d\}$

$v = e$
$D = \{0, 4, 7, 2, 5, 6\}$
$E = \{a, b, d, e\}$

$v = z$
$D = \{0, 4, 7, 2, 5, 6\}$
$E = \{a, b, d, e, z\}$

$v = c$
$D = \{0, 4, 7, 2, 5, 6\}$
$E = \{a, b, c, d, e, z\}$

$L(z) = 6$

5.
$V = \{a, b, c, d, e, z\}$
$E = \{(a, b, 3), (a, c, 7), (a, d, 4), (b, c, 2), (b, z, 9), (c, d, 1), (c, e, 3), (c, z, 6), (d, e, 3), (e, z, 3)\}

$a \rightarrow z$
$D = \{0, \infty, \infty, \infty, \infty, \infty\}$
$E = \{\}$

$v = a$
$D = \{0, 3, 7, 4, \infty, \infty\}$
$E = \{a\}$

$v = b$
$D = \{0, 3, 5, 4, \infty, 11\}$
$E = \{a, b\}$

$v = d$
$D = \{0, 3, 5, 4, 7, 11\}$
$E = \{a, b, d\}$

$v = c$
$D = \{0, 3, 5, 4, 7, 11\}$
$E = \{a, b, c, d\}$

$v = e$
$D = \{0, 3, 5, 4, 7, 10\}$
$E = \{a, b, c, d, e\}$

$v = z$
$D = \{0, 3, 5, 4, 7, 10\}$
$E = \{a, b, c, d, e, z\}$

$a \rightarrow z = 10$

6.
$a \rightarrow z$
$D = \{0, \infty, \infty, \infty, \infty, \infty, \infty, \infty\}$
$E = \{\}$

$v = a$
$D = \{0, 4, 3, \infty, \infty, \infty, \infty, \infty\}$
$E = \{a\}$

$v = c$
$D = \{0, 4, 3, 6, 9, \infty, \infty, \infty\}$
$E = \{a, c\}$

$v = b$
$D = \{0, 4, 3, 6, 9, \infty, \infty, \infty\}$
$E = \{a, b, c\}$

$v = d$
$D = \{0, 4, 3, 6, 9, 11, \infty, \infty\}$
$E = \{a, b, c, d\}$

$v = e$
$D = \{0, 4, 3, 6, 9, 11, 14, \infty\}$
$E = \{a, b, c, d, e\}$

$v = f$
$D = \{0, 4, 3, 6, 9, 11, 13, 18\}$
$E = \{a, b, c, d, e, f\}$

$v = g$
$D = \{0, 4, 3, 6, 9, 11, 13, 17\}$
$E = \{a, b, c, d, e, f, g\}$

$v = z$
$D = \{0, 4, 3, 6, 9, 11, 13, 17\}$
$E = \{a, b, c, d, e, f, g, z\}$

$a \rightarrow z = 17$

7.
A simple graph with 100 vertices, and an edge between every pair of distinct vertices, has
$99 + 98 + 97 \dots + 1$ vertices

The sum of integers from 1 to $n$ is given by the formula $\frac {n(n+1)}{2}$
$n = 99$
$\frac {99(99+1)}{2} = 99*50 = 4950$

A tree of $m$ vertices has $m-1$ edges, with $m = 100$,  so the tree has $99$ edges.
$4950 - 99 = 4851$ edges to be removed


7.
$E = V - 1$
$V = I + L$
so
$E = (I + L) - 1$

In a full binary tree, each internal vertex has exactly 2 children, so
$E = 2I$

therefore,
$2I = (I+L)-1$
Rearranging,
$I = L - 1$

Thus,
$L = 25$
$I = 24$
$V = 49$



