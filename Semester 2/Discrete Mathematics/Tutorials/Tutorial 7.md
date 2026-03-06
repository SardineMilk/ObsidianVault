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

