1.
$U = \{1, 2, 3, 4, 5, 6, 7, 8\}$
$A = \{1, 2, 7\}$
$B =\{1, 3, 6, 8\}$
$C = \{2, 5, 7\}$

a)
$C-A = \{5\}$   
$A - C = \{1\}$

b)
$A \cap \bar B = \{2, 7\}$

c)
$(A \cap B) \cup \bar C = \{1, 3, 4, 6, 8\}$

d)
$\overline {A \cap B} = \{2, 3, 4, 5, 6, 7, 8\}$

e)
$\overline {(C - A)} \cap B = \{1, 3, 6, 8\}$

f)
$A \bigtimes C = \{(1, 2), (1, 5), (1, 7), (2, 2), (2, 5), (2, 7), (7, 2), (7, 5), (7, 7)\}$


2.
$U = \{1, 2, 3, 4, 5, 6, 7, 8\}$
$A = \{1, 2, 7\}$
$B =\{1, 3, 6, 8\}$

$A \cap B = \{1\}$
$\overline {A \cap B} = \{2, 3, 4, 5, 6, 7, 8\}$

$\bar A = \{3, 4, 5, 6, 8\}$
$\bar B = \{2, 4, 5, 7\}$
$\bar A \cup \bar B = \{2, 3, 4, 5, 6, 7, 8\}$

$\overline {A \cap B} = \bar A \cup \bar B$


3.
a)
$A \cup B  = A$ implies $B \subset A$

b)
$A \cap B  = A$ implies $A \subset B$

c)
$A \textbackslash B = A$ implies $A \cap B = \emptyset$


4.
$U = \{1, 2, 3, 4, 5, 6, 7\}$
$A = \{2, 3, 4, 5\}$
$B = \{1, 5, 6\}$

$A = 0111100$
$B = 1000110$
$A \cap B = 0000100$
$A \cup B = 1111110$

5.
$A = \{1, \{1\}, \{2\}, 3\}$

a) $1 \in A$ T
b) $1 \subset A$ F
c) $\{1\} \in A$ T
d) $\{1\} \subset A$ T
e) $\{\{1\}\} \subset A$ T
f) $2 \in A$ F
g) $\{2\} \in A$ T
h) $\{2\} \subset A$ F
i) $\{3\} \in A$ F
j) $\{3\} \subset A$ T

6.
Let $P(n)$ be the statement $1 + 2^1 + 2^2 + 2^3 + ... + 2^n = 2 ^ {n + 1} - 1$

$P(1)$ states:
$1 + 2^1 = 2^ {1 + 1} - 1$
$3 = 2^2 - 1$
$3 = 4 - 1$
This is true, therefore $P(1)$ holds

Assume $P(k)$ holds for some $k$: $1 + 2^1 + ... + 2^k = 2 ^ {k + 1} - 1$
Then $P(k+1)$: 
$1 + 2^1 + ... + 2^k + 2 ^ {k + 1} = 2^{k+2} - 1$
The left hand side of $P(k+1)$ is:
$1 + 2^1 + ... + 2^k + 2 ^ {k + 1}$ 
$= [2 ^ {k + 1} - 1] + 2^{k+1}$
$= 2^{k+1} + 2^{k+1} - 1$
$= 2 * 2^{k+1} - 1$
$= 2^{k+2} - 1$
This matches the right hand side, so $P(k+1)$ holds
Thus, we see that $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$


7.
Let $P(n)$ be the statement $a_n = 2^{n+1} - 1$

$P(1)$ states:
$3 = 2^{1+1} - 1$
$3 = 4 -1$
This is true, so $P(1)$ holds

Assume $P(k)$ is true:
$a_k = 2^{k+1} - 1$
Then we must show $P(k+1)$ holds:
$a_{k+1} = 2^{k+2} - 1$
Using the recursive definition:
$a_{k+1} = 2a_k + 1$
$a_{k+1} = 2(2^{k+1}-1) + 1$
$a_{k+1} = 2^{k+1} - 2 + 1$
$a_{k+1} = 2^{k+1} - 1$
This matches the required formula

Thus, we see that $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$


8.
Let $P(n)$ be the statement $2 | n * (n + 1)$
$P(1)$ states 
$2|1*(1+1)$
$2|1*2$
$2|2$
This is true, so $P(1)$ holds

Assume $P(k)$ is true: 
$2|k*(k+1)$
So there exists some integer $m$ such that
$k * (k + 1) = 2m$
Since $P(k)$ holds:
$2|(k+1)*(k+2)$

$= k * (k+1) + 2 * (k+1)$
$= 2m + 2 * (k+1)$
$= 2 (m + (k+1))$
Both $m$ and $k$ are integers, so $m + (k+1)$ is an integer
Since $m + (k+1)$ is an integer,  $(k+1)*(k+2)$ is divisible by 2,
so $P(k+1)$ holds

Thus, we see that $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$


9.
$s_n = 1(1!) + 2(1!) +3(3!) +...+n(n!)$
1, 5, 23, 119
1, 2,  3,       4
$(n+1)! - 1$
$(n! * (n+1)) - 1$

Let $P(n)$ be the statement $1(1!) + 2(1!) +3(3!) +...+n(n!) = (n+1)! - 1$
$P(1)$ states that $1(1!) = (n + 1)! - 1$
- $1 = 2! - 1$
- This is true

Assume $P(k)$ is true:
$1(1!)+...+k(k!) = (k+1)! - 1$
Then we must show $P(k+1)$
$1(1!)+...+k(k!)+(k+1)((k+1)!) = (k+2)! - 1$

$1(1!)+...+k(k!)+(k+1)((k+1)!)$
$= [(k+1)! - 1] + (k+1)((k+1)!)$
$= (k+1)! - 1 + (k+1)((k+1)!)$
$= (k+1)!(1+(k+1)) - 1$
$= (k+1)!(k+2) - 1$
$= (k+2)! - 1$
This matches the right hand side
Thus, we see that $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$



10.
Let $P(n)$ be the statement $5 | 6^n - 1$

$P(1)$ states that $5|6^1 - 1$
- $5 | 6 - 1$
- $5|5$
- This is true, so $P(1)$ holds

Assume $P(k)$ is true:
$5 | 6^k - 1$
So there exists some integer $m$ such that
$6^k - 1 = 5m$
Since $P(k)$ holds,
$5 | 6^{k+1} - 1$
$5 | 6^k * 6 - 1$

$6^k * 6 - 1$ 
$= 6(6^k-1)+5$
$= 6(5m) + 5$
$= 30m + 5$
$= 5(6m+1)$
Since $6m+1$ is an integer, $6^{k+1}-1$ is divisible by 5
Thus, $P(k+1)$ holds

Therefore, we see $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$
