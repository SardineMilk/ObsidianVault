16:10 - 

1.
Let $f(n)$ be the statement that $5|6^n-1$
$f(1)$ states that $5|6^1 - 1$, 
$5|5$, which is true so $f(1)$ holds

Assume $f(k)$ holds for any natural number $k$
Therefore, there exists some integer $m$ such that
$5m = 6^k -1$

$f(k+1)$ states that $5|6^{k+1} - 1$
$= 6(6^k - 1) + 5$
$= 6(5m) + 5$
$= 30m + 5$
$= 5(6m + 1)$
Since $m$ is an integer, $6m+1$ is an integer, and $5(6m+1)$ is divisible by 5,
therefore $f(k+1)$ follows from $f(k)$
By the principle of mathematical induction, $f(n)$ holds for any positive integer $n$


2.
Choose unordered subsets of 2, 3, or 5 from a set of 15

$\frac {n!}{(n-k)! * k!}$
$\frac {15!}{(15-2)! * 2!}+\frac {15!}{(15-3)! * 3!}+\frac {15!}{(15-5)! * 5!}$
$\frac {15!}{(13)! * 2}+\frac {15!}{(12)! * 6}+\frac {15!}{(10)! * 120}$


3.
$P$ = punk rock likers
$R$ = reggae likers 
$T$ = techno likers 

$|P| = 12$
$|R| = 26$
$|T| = 31$

$|U| = 99$

$|P \cap R| = 7$
$|P \cap T| = 6$
$|R \cap T| = 12$
$|\bar P \cap \bar R \cap \bar T| = 51$

a)
$|P \cup T| = |P| + |T| - |P \cap T|$
$|P \cup T| = 12 + 31 - 6 = 37$

b)
$|P \cup T \cup R| = |U| - |\bar P \cap \bar R \cap \bar T|$
$= 99 - 51 = 48$

c)
$|P \cup T \cup R| = |P| + |T| + |R| - |P \cap R| - |P \cap T| - |R \cap T| + |P \cap T \cap R|$
$48 = 12 + 31 + 26 - 7- 6 - 12 + x$
$48 = 69  - 25 + x$
$48 = 44 + x$
$x = 4$

4.

5.
Both Prim's and Kruskal's start by choosing the minimum weight edge in the graph
They then proceed by adding minimum weight edges that don't form a circuit with already added edges, until $n-1$ edges have been added to the tree.
The difference is that Prim's only considers edges incident to those already in the tree, while Kruskal's considers all in the graph

Each row is the edge added in that iteration
(a, c)
(c, h)
(h, g)
(h, f)
(f, d)
(d, e)
(a, b)
(b,i)

6.
In a tree
E = V - 1
V = I + L

In a full binary tree
E = 2I

640 = 2I 
I = 320

V = 320 + L
640 = (320+L) - 1$
L = 321

7.
a
c
b
d
e
f
g
z
17

8.
a)
0 0 1 1
1 0 1 0
0 1 0 0
0 1 0 1

b)
$0*0 + 0*0 + 1*1 + 1*1 = 2$
2 directed paths of length 2 from a to b 

c)
yes it is strongly connected


9.
$a_n = a_{n-1} + 6a_{n-2}$


10.

$$\begin{bmatrix}
1 & 2 & -2 & 3 & |6 \\
2 & 4 & -3  & -2 & |14 \\
3 & 6 & -4 & -7 & |22
\end{bmatrix}$$

$R_2 \rightarrow R_2 - 2R_1$ 
$$\begin{bmatrix}
1 & 2 & -2 & 3 & |6 \\
0 & 0 & 1  & -8 & |2 \\
3 &6 & -4 & -7 & |22
\end{bmatrix}$$
$R_3 \rightarrow R_3 - 3R_1$ 
$$\begin{bmatrix}
1 & 2 & -2 & 3 & |6 \\
0 & 0 & 1  & -8 & |2 \\
0 & 0 & 2 & -16 & |4
\end{bmatrix}$$
$R_3 \rightarrow R_3 - 2R_2$
$$\begin{bmatrix}
1 & 2 & -2 & 3 & |6 \\
0 & 0 & 1  & -8 & |2 \\
0 & 0 & 0 & 0 & |0
\end{bmatrix}$$
$x + 2y - 2z + 3w = 6$
$z - 8w = 2$

$x = 10 + 13w - 2y$
$z = 2 + 8w$
with $w$ and $y$ as free variables