Geometric
- depends on $a_{n-1}$ or similar
Algebraic
- Doesnt
- Also called *Closed Form*
### Closed Form
Represent a recurrence relation in terms of $n$, without $n{-1}$ of similar
Not all recurrence relations have this form

**Example**
$a_n = 2a_{n-1} + 1,  n \geq 2$
$a_1 = 1$
Verify the solution is $a_n = 2^n - 1$

$n = 1,$ 
$a_1 = 2 - 1$
$= 1$
This is true, so $a_n = 2^n$ matches the recurrence relation for the base case of $n=1$

$n \geq 2$
$a_{n-1} = 2^{n-1} - 1$ *closed form for n-1*
$a_{n} = 2 * (2^{n-1} -1) + 1$ *sub it into n-1 in the recurrence relation for n*
$= 2^n - 2 + 1$ *simplify*
$= 2^n - 1$ *show it is equal to closed form for n*

**Example**
$a_{n+1} = 1.04 * a_n$
Closed form:
$a_{n+1} = a_1 * 1.04^n$

**Example**
Tower of Hanoi

Let $a_n$ be the minimal number of moves to solve the puzzle with $n$ disks

To move $n$:
Move $n-1$ to $B$
Move $n$'th to $C$
Move $n-1$ to $C$
$a_n = a_{n-1} + 1 + a_{n-1}$

$a_n = a_{n-1} + 1 + a_{n-1}$
$a_n = 2(a_{n-1}) + 1$
$a_n = 2^m - 1$

**Example**
Climb a set of $n$ stairs, taking either 1 or 2 at a time

1: 1
2: 2
3: 3

$a_n = a_{n-1} * 1 + a_{n-2} * 1$
$a_n = a_{n-1} + a_{n-2}$

### Linear and Homogeneous
#### Linear
No powers

$a_n = 2 a_{n-1} + 1$
$b_n = 5 b_{n-1} - 2 b_{n-2}$

#### Homogeneous
$a_n = 0.5 a_{n-1}$

Only multiples of $a_n-1$, $a_{n-2}$ etc


#### Solving Homogeneous
Consider the geometric sequence
$a_n = p a_{n-1}$
$a_0, p a_0, p^2 a_0, p^3 a_0, ...$
where $a_0$ is the initial condition, $a_0 = c$
$a_n = c * p^n$


Relations of the form $a_n = 7a_{n-1} - 12a_{n-2}$
assume $a_n = r^n$ is a solution
$r_n = 7 r^{n-1} - 12 r^{n-2}$
$r^2 = 7r - 12$ *dividing by $r^{n-2}$*
$r^2 - 7r + 12 = 0$
$(r - 4)(r-3) = 0$
$r = 4$ or $r = 3$
So
$a_n = 3^n$ and $a_n = 4^n$
so
$a_n = c*3^n + d * 4^n$
where $c, d \in \mathbb{R}$ (constants)

In general, when the characteristic equation has two distinct real solutions
The general solution of 
$a_n = p a_{n-1} + q a_{n-2}$
is
$a_n = c(r_1)^n + d(r_2)^n$

Where $r_1, r_2$ are solutions of the characteristic equation $r^2 = pr + q$
and $c, d$ are constants determined by the initial conditions


If the char equ has a repeated root, $r = r_1$
then the general solution of the RR $a_n = p a_{n-1} + q a_{n-2}$
is
$a_n = c * {r_1}^n + d * n * {r_1}^n$


#### Solving Inhomogeneous Recurrence relations
Involves a term free of $a_{n-x}$
Example: $a_n = 4 a_{n-1} - 15$

**Solving:**
*Find the general solution of the homogeneous r.r*
$a_n = 4 a_{n-1}$

*Find a particular solution of the same form as the homogeneous solution*
(Make an educated guess of what might be a solution)

(sub into r.r)
$p = 4p - 15$
-15 is constant so take
$a_n = p, p \in \mathbb{R}$
$p = 5$
so $a_n = 5$

*Add the solutions from parts 1 and 2*
$a_n = c * 4^n + 5$

**Example**
$a_n = 3 a_{n-1} + 9 - 2_n$

*find homogeneous solution*


