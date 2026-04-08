1.
$R = \{(a, b) | a \neq b \}$

If $R$ is reflexive, then for every $a$ in $R$, $(a, a)$ is in $R$
$a = a$, therefore $(a, a)$ cannot be in $R$
Therefore $R$ is not reflexive

If $(a, b)$ if in $R$, $a \neq b$, then $b \neq a$ therefore $(b, a)$ is in $R$ 
Therefore $R$ is symmetric

By the same logic, $R$ is not antisymmetric

If $(a, b)$ and $(b, c)$ in $R$ and $a = c$, then $(a, c)$ is not in $R$
Therefore $R$ is not transitive

2.
i)
If $a = a$, then they're the same age, so $R$ is reflexive
If $a$ is the same age as $b$, then $b$ is the same age as $a$, so $R$ is symmetric
If $a$ is the same age as $b$, then $b$ is the same age as $a$, $a \neq b$, both $(a, b), (b, a) \in R$, so $R$ is not antisymmetric
If $a$ is the same age as $b$, and $b$ is the same age as $c$, then $c$ is the same age as $a$, so $R$ is transitive

ii)

3.
i imagined it with my vivid and detailed imagination

4.
$R = \{(a, a), (a, b), (b, a), (b, b), (c, a), (c, d), (d, d)\}$
a)
$(c, c) \notin R$, so $R$ is not reflexive
$(c, a) \in R$, $(a, c) \notin R$, so $R$ is not symmetric
$(c, a) \in R$, $(a, b) \in R$, $(c, b) \notin R$, so $R$ is not transitive

b)
$R = \{(a, a), (a, b), (b, a), (b, b), (c, a), (c, c), (c, d), (d, d)\}$

c)
$R = \{(a, a), (a, b), (a, c), (b, a), (b, b), (c, a), (c, d), (d, c) (d, d)\}$

5.
$dr(n):$
Add up all digits
Repeat until you obtain a single digit number

Domain: $\mathbb{N}$
Codomain: $\{1, 2, 3, 4, 5, 6, 7, 8, 9\}$

This function is surjective, as every element of the codomain has at least one corresponding element in the domain
The function is not injective as multiple elements in the domain can map onto one element in the codomain
$dr * dr = dr$

6.
$f(x) = 4x - 3, g(x) = x^2 + 1,$ $h(x) =$ 1 if x>=0, 0 if x<0

a)
$g(f(x))$
$= g(4x-3)$
$= (4x-3)^2 + 1$
$= 16x^2 - 24x + 10$

b)
$f(g(x))$
$= f(x^2+1)$
$=  4(x^2+1)-3$
$= 4x^2 + 1$

c)
$f(f())$
$= f(4x-3)$
$= 4(4x-3)-3$
$= 16x - 15$

d)
$h(h()) = 1$

e)
$g(h())$
= 2 if x>= 0, 1 if x<0

7.
Find the inverse or explain why none exists

a)
$f: \mathbb{N} \rightarrow \mathbb{N}, f(x) = 5x - 2$
This function is injective, as no two values of $x$ map to the same element on the codomain
However, the function is not surjective, as the domain only maps to values that are 2 less than a multiple of 5 in the codomain
Therefore, the function is not invertible

b)
$f: \mathbb{R} \rightarrow \mathbb{R}, f(x) = 5x - 2$
This function is injective, as no two values of $x$ map to the same element on the codomain
The function is also surjective, as unlike the natural numbers, every real number has a real number that is $(x+2)/5$
Therefore, the function is invertible

c)