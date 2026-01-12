1.
*Show that for any sets $A$ and $B$*:
a)
$\overline {A \cup B} = \bar A \cap \bar B$

Assume
$x \in \bar A \cap \bar B$
Then
 $x \in \bar A$ and $x \in \bar B$
Which means
 $x \notin A$ and $x \notin B$
 Which means
 $x \notin A \cup B$
 So
 $x \in \overline {A \cup B}$

Assume
 $x \in \overline {A \cup B}$
 Then
 $x \notin A \cup B$
 Which means
 $x \notin A$ and $x \notin B$
 Which means
 $x \in \bar A$ and $x \in \bar B$
 So
 $x \in \bar A \cap \bar B$


b)
$\overline {A \cap B} = \bar A \cup \bar B$

Assume
$x \in \bar A \cup \bar B$
Then
 $x \in \bar A$ or $x \in \bar B$
 Which means
 $x \notin A$ or $x \notin B$
 Which means
 $x \notin A \cap B$
 So
 $x \in \overline {A \cap B}$
 
Assume
 $x \in \overline {A \cap B}$
Then
 $x \notin A \cap B$
 Which means
 $x \notin A$ or $x \notin B$
 Which means
 $x \in \bar A$ or $x \in \bar B$
 So
$x \in \bar A \cup \bar B$
 
2.
Let $P(n)$ be the statement $3^n > 2^{n+1}$

$P(2)$ states:
$3^2 > 2^{2+1}$
$3^2 > 2^3$
$9 > 8$
This is true, so $P(2)$ holds

Assume $P(k)$ is true:
$3^k > 2^{k+1}$
We must show that
$3^{k+1} > 2^{k+2}$
$3^k * 3 > 2^{k+1} * 2$
$3^k * 3/2 > 2^{k+1}$
Since we have already shown that $3^k > 2^{k+1}$,
and $3^k * 3/2$ is larger, $P(k+1)$ holds

Therefore, $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for any $n \geq 2$

3.
Let $P(n)$ be the statement $3|2^n * 2^n - 1$

$P(1)$ states:
$3 | 2^1 * 2^ 1 -1$
$3|2 * 2 - 1$
$3 | 4 - 1$
This is true, so $P(1)$ holds

Assume $P(k)$ is true:
$3 | 2^k * 2^k - 1$
So there exists some integer $m$ such that
$2^k * 2^k - 1 = 3m$
Since $P(k)$ holds:
$3 | 2^{k+1} * 2^{k+1} - 1$
$3 | 2 * 2^{k} * 2 * 2^{k} - 1$
$3 | 4 * 2^{k} * 2^{k} - 1$

$4 * 2^{k} * 2^{k} - 1$ 
$= 4(2^k * 2^k)−1$
$= 4(3m+1)−1$
$= 12m + 4 - 1$
= $12m + 3$
= $3(4m+1)$

Since $4m+1$ is an integer $4 * (2^{k} * 2^{k}) - 1$ is divisible by 3,
so $P(k+1)$ holds

Therefore, $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for any $n$

*I think this proof is incorrect. I proved the number of squares is divisible by 3, not that the board is tileable*



