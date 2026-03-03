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


##### 1.5.1
$A = \{2, 3, 4, 5, 6\}$
$R = \{(a,b)\in A \times A| a \space divides \space b\}$
$R = \{(2, 4), (2, 6), (3, 6)\}$

##### 1.5.2
$R = \{(a, b)\in \mathbb{R} | a \leq b \}$

Is $R$ reflexive?
$a \leq a$, so $(a, a)$ is in $R$
So $R$ is reflexive.

Is $R$ symmetric?
Take two elements of $\mathbb{R}$, $a$ and $b$,  with $a < b$
$a \leq b$, so $(a, b)$ is in $R$
but $b \leq a$ is false, so $(b, a)$ is not in $R$
So $R$ is not symmetric.

Is $R$ antisymmetric?
If both $(a, b)$ and $(b, a)$ are in $R$, then
$a \leq b$, and $b \leq a$, 
which implies $a = b$
So $R$ is antisymmetric.

Is $R$ transitive?
If $a \leq b$ and $b \leq c$, then $a \leq c$
So $R$ is transitive.

##### 1.5.3
$A = \{1, 2, 3\}$
$R = \{(1, 2), (2, 2), (2, 3)\}$

$R_r = \{(1,1), (1, 2), (2, 2), (2, 3), (3,3)\}$
$R_s = \{(1, 2), (2,1), (2, 2), (2, 3), (3,2)\}$
$R_t = \{(1, 2), (1, 3), (2, 2), (2, 3)\}$


##### 1.6.1
For each function, find its range
Determine if its *surjective* and/or *injective* 
$X$ is the set of all finite non empty bit strings
$Y$ is the set of all non-negative integers

a)
$f: \mathbb{R} \rightarrow \mathbb{R}, f(x) = 2x + 1$
The range is $\mathbb{R}$
The range is equal to the codomain, so $f$ is *surjective*
Every element of the codomain has exactly one corresponding element of the domain, 
so $f$ is *injective*

b)
$g: \mathbb{R} \rightarrow \mathbb{R}, g(x) = x^4 + 1$
The range is $y \in \mathbb{R}, y>=1$
The range is not equal to the codomain, so $g$ is *not surjective*
The function is symmetric on the $y$ axis. $x, -x$ produce the same output
Therefore, it is *not injective*

c)
$h: X \rightarrow Y, h(s) =$ number of ones in $s$

For some integer $s$, the string consisting of $s$ ones is in $X$
Therefore, it is *surjective*
The bit strings $1$ and $01$ produce the same output (1)
Therefore, $h$ is *not injective*

d)
$j : X \rightarrow Y, j(s) =$ the first bit of $s$
The first bit of $s$ may only be $0$ or $1$, therefore $j$ is *not surjective*
Any bit string beginning with $0$ will produce the output $0$, therefore it it *not injective*

##### 1.6.2
$f, g, h$ have $\mathbb{R}$ as their domain and codomain
$f(x) = 4x-3$
$g(x) = x^2 + 1$
$h(x) = x \geq 0 ? 1:0$

a)
$f \circ f = f(f(x)) = f(4x-3) = 4(4x - 3) - 3 = 16x - 15$
b)
$h \circ f = h(f(x)) = h(4x-3) = x \geq 3/4 ? 1:0$
c)
$h \circ g = h(g(x)) = h(x^2 + 1) = (x^2+1) \geq 0?1:0 = x^2 \geq -1 ? 1:0 = 1$

##### 1.6.3
Find the inverse function for:
a)
$g: \mathbb{R} \rightarrow \mathbb{R}, g(x) = \sqrt{x^2}$
$x$ and $-x$ produce the same output: $x$
Therefore, $g$ is not injective
Since a function is invertible if and only if it is bijective, $g$ is not invertible

b)
$j: S \rightarrow S$
$S =$ The set of non-empty finite strings of lower case letters
$j(s) =$ move the last character to the beginning of the string

Inverse:
$j(s) =$ move the beginning character to the end of the string


##### 1.7.1
How many binary words with length 7?
$2*2*2*2*2*2*2 = 128$
Length 1 2 or 3?
$(2) + (2 * 2) + (2*2*2) = 14$

##### 1.7.2
A salesman visits 5 towns once each. How many possible orders?
$5*4*3*2*1 = 120 = 5!$ 

##### 1.7.3
How many numbers between 1 and 1000 have exactly one 7?

$**7$
Units - 1 number
Tens - 9 numbers
Hundreds - 9  numbers
$1 * 9 * 9 = 81$

$*7*$
Units - 9 numbers
Tens - 1 number
Hundreds - 9 numbers
$9 * 1 * 9 = 81$

$7**$
Units - 9 numbers
Tens - 9 numbers
Hundreds - 1 numbers
$9 * 9 * 1 = 81$

$81+81+81 = 243$


##### 1.8.1
How many ways can a subset of one or two elements be picked from a set on $n$ elements?

$\binom {n}{1} = \frac{n!}{(n-1)!*1!} = \frac{n!}{(n-1)!} = n$
$\binom {n}{2} = \frac{n!}{(n-2)!*2!} = \frac{n!}{(n-2)! * 2}$
$\frac{n!}{(n-2)! * 2} + n$
$= 0.5 * n * (n+1)$

##### 1.8.2
A university has 12 male professors and 3 female professors.
How many committees of 12 people containing at least one female member?

$\binom{3}{1} = \frac{3!}{(3-1)!*1!} = 3$
$\binom{12}{11} = \frac{12!}{(12-11)!*11!} = 12$
$3 * 12 = 36$

$\binom{3}{2} = \frac{3!}{(3-2)!*2!} = 3$
$\binom{12}{10} = \frac{12!}{(12-10)!*10!} = 66$
$3 * 66 = 198$

$\binom{3}{3} = \frac{3!}{(3-3)!*3!} = 1$
$\binom{12}{9} = \frac{12!}{(12-9)!*9!} = 220$
$1 * 220 = 220$

$36 + 198 + 220 = 454$

##### 1.8.3
20 undergrads, 10 postgrads
Pick 5 where:

Any team is valid
$\binom{30}{5} = \frac{30!}{(30-5)! * 5!} = 142,506$
There must be 2 postgrads and 3 undergrads
$\binom{20}{3} = \frac{20!}{(20-3)! * 3!} = 1140$
$\binom{10}{2} = \frac{10!}{(10-2)! * 2!} = 45$
$1140 * 45 = 51300$

##### 1.8.4
How many ways to pick $k$ distinct numbers from $\{1, 2, \dots, n\}$, if 1 and 2 cannot both be picked?

Either:
Pick $k$ from $3-n$ inclusive:  $n-2$ choose $k$
Pick $k-1$ from $3-n$, and $1$:  $n-2$ choose $k-1$
Pick $k-1$ from $3-n$, and $2$:  $n-2$ choose $k-1$

$\binom{n-2}{k} = \frac{(n-2)!}{(n-2-k)!*k!}$
$\binom{n-2}{k-1} = \frac{(n-2)!}{(n-2-(k-1))!*(k-1)!}$

$\binom{n-2}{k} + 2\binom{n-2}{k-1}$
$\frac{(n-2)!}{(n-2-k)!*k!} +  \frac{2(n-2)!}{(n-2-(k-1))!*(k-1)!}$


##### 2.1.1
Find outcomes, state if they are equiprobable
a)
A red, blue and a yellow ball are put into a bag and a ball is draw out at random
$S = \{red,blue,yellow\}$
1/3, 1/3, 1/3
They are equiprobable

b)
two yellow balls, one red, one blue
$S = \{y, y, r, b\}$
$2/4, 1/4, 1/4$
They are not equiprobable

c)
two yellow balls, one red, one blue
Draw two balls
y, y, r, b
$S = \{(y,y),(y,r),(y,b),(y,r),(y,b),(r,b)\}$
1/6, 2/6, 2/6, 1/6
The outcomes are not equiprobable

##### 2.12
Prove that if $A \subset B$, then $P(A) \leq P(B)$

If $A \subset B$ (A is a subset of B)
Then 
$B = A \cup (B - A)$

$A$ and $B - A$ are disjoint, so
$P(B) = P(A) + P(B - A)$

Probability must be non negative : $0 \leq P(x) \leq 1$
$P(B-A) \geq 0$

Therefore
$P(A) \leq P(A) + P(B-A)$
and
$P(B) = P(A) + P(B - A)$
So
$P(A) \leq P(B)$

##### 2.1.3
Rain Today
$P(A) = 0.3$

Rain Tomorrow
$P(B) = 0.4$

Rain Today and Tomorrow
$P(C) = 0.2$

Rain Tomorrow but not Today
$P(B \cap \bar A)$

$B = (B \cap A) \cup (B \cap \bar A)$
$P(B \cap \bar A) = P(B) - P(B \cap A)$
$= 0.4 - 0.2 = 0.2$


##### 2.1.4
$P(A) = 0.75$
$P(B) = 0.65$

If $A$ and $B$ were mutually exclusive, then:
$P(A) + P(B) = P(A \cup B)$
$P(A \cup B) = 0.65 + 0.75 = 1.4$
$A, B \subset S$
$P(S) = 1$
$1.4 > 1$, therefore $A$ and $B$ cannot be mutually exclusive


##### 3.1.1
Verify that the solution of 
$a_n = 5a_{n-1} -12$
$a_1 = 13$
is
$a_n = 2(5)^n + 3$

*Prove base case*
$a_1 = 2(5)^1 + 3 = 10 + 3 = 13$
$a_1 = 13$ 
This is true, so the given formula is correct for the initial value
*Induction step*
$a_{n+1} = 2(5)^{n+1} + 3$
$5a_{n} - 12 = 2(5)^{n+1} + 3$
$5a_{n}= 2(5)^{n+1} + 15$
$a_{n}= 2(5)^{n} + 3$
so the given formula is correct

##### 3.1.2
$x_n = \frac {2nx_{n-1}}{n+1}$
$x_1 = 1$

a)
$a_n = (n+1)x_n$
$a_1 = 2$
prove
$a_n = 2a_{n-1}$


##### 3.2.1
$a_n = 6a_{n-1} - 5a_{n-2}$
$a_1  = 1$
$a_2 = 41$

$a_n = 6a_{n-1} - 5a_{n-2}$
$t^2 - 6t + 5 = 0$
$(t - 5)(t - 1) = 0$
$r1, r2 = 5, 1$
$a_n = C(5)^n + D(1)^n$

$1 = C5^1 + D$
$41 = C5^2 + D$

$1 = 5C + D$
$41 = 25C + D$

$40 = 20C$
$C = 2$
$1 = 5 (2) + D$
$1 = (10) + D$
$D = -9$

$a_n = 2 * 5^n - 9$




##### 3.4.1
How many ternary (0, 1,2) strings of length $n$ don't have two consecutive 0's?


| $n$ | $a_n$ |
| --- | ----- |
| 1   | 3     |
| 2   | 8     |
| 3   | 22    |
| 4   | 60    |
| 5   | 164   |
| 6   | 448   |
What is the last character of a string of length $a_n$ ?
1/2:
- $2 a_{n-1}$ options for the string
0:
- Previous character must be 1/2, or it would be invalid
- $2a_{n-2}$ options

$a_n = 2 (a_{n-1} + a_{n-2})$
$a_1 = 3$
$a_2 = 8$

$a_3 = 22$
$a_4 = 60$
$a_5 = 164$
$a_6 = 448$

##### 3.42
How many regions are formed if you draw $n$ lines in a plane
No 2 lines are parallel
No 3 lines pass the same point

$a_1 = 2$
$a_2 = 4$

$a_3 = 7$
$a_4 = 11$

$a_n = a_{n-1} + n$

