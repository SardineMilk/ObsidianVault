##### 1.1.1
List the elements of the set {x | x is the square of an integer and x < 25}
- $A$ = {x | x is the square of an integer and x < 25}
- $A = \{0,1, 4, 9,16\}$

##### 1.1.2
$A = \{1, 2, 3\}, B= \{x, y\}$
Find $B \bigtimes A$
- $B \bigtimes A = \{(x, 1), (x, 2),  (x, 3), (y, 1), (y, 2), (y, 3)\}$


##### 1.2.1
$U = \{1, 2, 3, 4, 5, 6, 7, 8\}$
$A = \{3, 8\}$
$B = \{2, 4, 6, 8\}$
$C = \{1, 3, 5, 7\}$

$C \textbackslash A = \{1, 5, 7\}$
$A \cap \bar B = \{3\}$
$(A \cap B) \cup \bar C = \{2, 4, 6, 8\}$
$\overline {(A \cap B)} = \{1, 2, 3, 4, 5, 6, 7\}$
$\overline {(C \textbackslash A)} \cap B = \{2, 4, 6, 8\}$

##### 1.2.2
$C = A \cap \bar B$
$D = A \cap B$
$C \cap D = \{ \}$


##### 1.3.1
$U = \{1, 2, 3, 4, 5, 6, 7\}$
$A = \{3, 4, 5, 7\}$
$B = \{5, 6\}$

$A$ = 0011101
$B$ = 0000110
$\bar A$ = 1100010 
$A \cup B$ = 0011111
$A \cap B$ = 0000100

##### 1.3.2
a - The empty set
b - The finite universal set $U$

##### 1.3.3
An index in $A \textbackslash B$ should be 1 if it is 1 in $A$ and 0 in $B$
So,
For any 1's in $B$, set the corresponding index of $A$ to 0
or more formally:
$A \textbackslash B = A \cap \bar B$


##### 1.4.1
Let $P(n)$ be the statement $3n - 100 \geq 0$

$P(1)$ states that $(3 * 1) - 100 \geq 0$. This is false.
$P(4)$ states that $(3 * 4) - 100 \geq 0$. This is false.
$P(40)$ states that $(3 * 40) - 100 \geq 0$. This is true.

##### 1.4.2
Let $\{a_n\}$ be the sequence defined by $a_1 = 3$ and
$a_{n+1} = 5a_n − 8 , n ≥ 1$.
Let $P(n)$ be the statement $a_n = 5^{n−1} + 2$. Write down $P(1)$ and $P(2)$ . Which of
them are true?

$P(1)$ states that $a_1 = 5^0 + 2$. This is true.
$P(2)$ states that $a_2 = 5^1 + 2$. This is true.

##### 1.4.3
Prove by induction that $3^n < n!$ for $n \geq 7$

Let $P(n)$ be the statement $3^n < n!$
$P(7)$ states that $3^7 < 7!$
- $2187 < 5040$
- This is true
Assume $P(k)$ is true: $3^k < k!$
Then 
- $3^{k + 1} < k! * (k + 1)$
- $(3^k) * 3 < k! * (k + 1)$
Since $k \geq 7$ and we have $k + 1 \geq 8 > 3$ , and therefore $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for all $n \geq 7$

##### 1.4.4
Let $\{a_n\}$ be the sequence defined by $a_1 = x$ and
$a_{n+1} = \frac {a_n^2 + 12}{7}, n \geq 1$
where $3 < x < 4$. 
Prove by induction that $3 < a_n < 4$ for all $n$.

$P(1)$ states that $3 < a_1 < 4$, which is true by assumption
Assume $P(k)$ is true: $3 < a_k < 4$
We must show $3 < a_{k+1} < 4$ is true
Since $a_k > 3$,  the lower bound is:
$a_{k+1} > \frac {3^2 + 12}{7}$
$a_{k + 1} > 3$
Since $a_k < 4$, the upper bound is:
$a_{k+1} < \frac {4^2 + 12}{7}$
$a_{k + 1} < 4$
Thus, $3 < a_{k+1} < 4$,
Therefore $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for all $n \geq 1$

##### 1.4.5
For $n \geq 2$ the sequence $\{s_n\} is given by **by**
$s_n = (1 - \frac {1}{2})(1 - \frac {1}{3}) ... (1 - \frac {1}{n})$
so that $s_2 = \frac {1}{2}$ and $s_3 = \frac {1}{3}$. By computing more values of $s_n$ if needed, guess a formula for $s_n$ and use induction to prove it.

$s_4 = 1/4$
$s_n = 1/n$

Let $P(n)$ be the statement $(1 - \frac {1}{2}) \dots (1 - \frac {1}{n}) = \frac{1}{n}$
$P(2)$ states $(1 - \frac {1}{2}) = \frac {1}{2}$
This is true, so $P(2)$ holds

Assume $P(k)$ is true:
$(1 - \frac {1}{2}) \dots (1 - \frac {1}{k}) = \frac{1}{k}$
We must show $P(k+1)$ is true:
$(1 - \frac {1}{2}) \dots (1 - \frac {1}{k})(1 - \frac {1}{k+1}) = \frac{1}{k+1}$
The left side is:
$(1 - \frac {1}{2}) \dots (1 - \frac {1}{k})$
$= [\frac {1}{k}](1 - \frac {1}{k+1})$
$= \frac {1}{k} * \frac {k}{k+1}$
$= \frac {1}{k+1}$
This matches the right hand side
 Thus, we see that $P(k+1)$ follows from $P(k)$
 By the principle of mathematical induction, $P(n)$ is true for  $n \geq 2$


