11:33

Part 1
1 C *3*
2 B *3*
3 D *3*
4 B *3*
5 C *3*
6 B *3*
*18/18*
11:37

11:43
Part 2
7 *8*
$f: \mathbb{N} -> \mathbb{N}$ 
$f(n) =$ (4 - n for n < 4) (n for n $\geq$ 4)

a) range of $f$
$1, 2, 3$ map to $3, 2, 1$ respectively
$4, 5, 6...$ map to $4, 5, 6...$
$f(n) \geq 1$

b) is $f$ surjective
If $f$ is surjective, the range is equal to the codomain.
The codomain is the natural numbers, integers greater than 0
This is equal to the range, therefore $f$ is surjective

c) is $f$ injective
If $f$ is injective, every element in the codomain has exactly one corresponding element in the domain.
Every $n \geq 4$ maps to the same number in the codomain
The elements 1, 2, 3 map to 3, 2, 1 respectively.
This is the case, therefore $f$ is injective

d) find inverse $f^{-1}$ or explain why there is none 
$f$ is surjective and injective, therefore there is an inverse function
$f^{-1} =$ (4 - n for n < 4) (n for n $\geq$ 4)
$f^{-1}$ is the same function as $f$

8 *6*
23 total objects
Type 1 
- 8
- 3 defective
Type 2
- 15
- 5 defective
$A$ is type 1
$B$ is defective

a)
$P(A) = 8/23$
$P(B) = 8/23$
b)
$P(A \cap B) = 3/23$
c)
$P(A|B) = P(A \cap B)/P(A) = (3/23)/(8/23) = 3/8$
$P(B | A) = P(A \cap B)/P(B) = (3/23)/(8/23) = 3/8$

9 *0/8*
Let the statement $P(n)$ be $3|(5 * 4^n + 1)$ 
That is, there exists some integer $m$ such that
$3m = 5* 4^n + 1$

$P(1)$ states that 
$3|(5 * 4^1 + 1)$
$3|21$
$3m = 21$
$m = 21/3 = 7$
$m$ is an integer, so $P(1)$ holds

Assume $P(k)$ holds  for some integer $k \geq 0$:
$3|(5 * 4^k + 1)$ 
That is, there exists some integer $m$ such that
$3m = 5* 4^k + 1$
We must show $P(k+1)$ also holds:
$3 | 5 * 4^{k+1} + 1$
$= 4 (5 * 4^k) +1$
$= 4(5 * 4^{k}+1) - 4 + 1$
$= 4(5 * 4^{k}+1) - 3$
$=4(3m) - 3$
$= 12m - 3$
$= 3(4m - 1)$

Since $m$ is an integer, $4m -1$ is also an integer, 
Therefore, $5 * 4^{k+1} + 1$ is divisible by 3 
*Notes - An integer times $3$ is equal to* $5 * 4^{k+1} + 1$

Thus, $P(k+1)$ follows from $P(k)$
By the process of mathematical induction, $P(n)$ holds for every positive integer $n$

12:05