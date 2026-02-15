### What is a Recurrence Relation?
Any recurrence relation can be expressed like this:
$a_n = f(a_{n-1}, a_{n-2}, \dots, a_1, a_0)$
Not all terms must be used by the function.
Most recurrence relations use one or two.
The number of terms used in the function is called the *order* of the recurrence relation.
- This will sometimes be referred to as $k$ in these notes, for clarity

The value used for the first values of the sequence will affect all other values in the sequence.
These are called the *initial conditions*
There are $k$ initial conditions for each sequence
- This is simpler than it sounds, try to understand it intuitively

> A recurrence relation defines a sequence, where the value of the $n_{th}$ term depends on $k$ preceding terms, and the initial $k$ terms.

**Examples:**
$a_n = 2a_{n-1} + 1$ 
$a_1 = 1$
*This is a simple recurrence relation, with an order of 1, and an initial condition of $a_1 = 1$*

$a_n = a_{n-1} + a_{n-2}$
$a_1 = 1$
$a_2 = 1$
*A famous recurrence relation called the Fibonacci Sequence. It has an order of 2, and the initial conditions $a_1 = 1, a_2 = 1$. If you change these initial conditions, the entire sequence changes*


### Types of Recurrence Relation
#### Linear vs Nonlinear
##### Linear
A recurrence is *linear* if each previous term has no powers and is not multiplied by previous terms
These are more common, and easier to solve

**General Form:**
$a_n = c_1 a_{n-1} +  c_2 a_{n-2} + \dots +  c_k a_{n-k} + g(n)$
The $c$ terms are constants
$g(n)$ is any value not dependant on previous terms
- This may be 0
- It may also be dependant on $n$

**Examples:**
$a_n = 2a_{n-1}$
$a_n = 2a_{n-1} + 1$
$a_n = 2a_{n-1} + 3a_{n-2}$
$a_n = 7a_{n-1} - 5a_{n-2} + 1$
$a_n = 1.5a_{n-1} - a_{n-2} + n$
$a_n = a_{n-1} + (n^2)/2 + n$

##### Nonlinear
*Nonlinear* recurrences have previous terms combined using multiplication, powers, roots etc.

**Examples:**
$a_n = a_{n-1}^2$
$a_n = a_{n-1}^2 + 1$
$a_n = a_{n-1} a_{n-2}$
$a_n = 1/a_{n-1}$
$a_n = \sqrt {a_{n-1}}$


#### Homogeneous vs Nonhomogeneous
##### Homogeneous
Only dependent on previous terms
No additional function of $n$

**Examples:**
$a_n = 2a_{n-1}$
$a_n = 2a_{n-1} + 3a_{n-2}$
$a_n = a_{n-1}^2$
$a_n = a_{n-1} a_{n-2}$
$a_n = a_{n-1}^2 + 6a_{n-2}$

##### Nonhomogeneous
Includes $g(n)$, an additional function of $n$

**Examples:**
$a_n = a_{n-1} + 1$
$a_n = a_{n-1} + n$
$a_n = a_{n-1}^2 + 1$
$a_n = 7a_{n-1} - 5a_{n-2} + 1$


### Solving Recurrence Relations
Solving recurrences can be difficult
There are different techniques for different types of recurrence relation

#### First Order Linear Homogeneous
**General Relation Form:**
$a_n = p * a_{n-1}$

**General Solution:**
The general solution of
$a_n = p * a_{n-1}$
Is
$a_n = c * p^n$
Where $c$ is a constant determined by the initial condition

**Example:**
$a_n = 2a_{n-1}$
$a_1 = 1$

$a_n = c * 2^n$
$1 = c * 2^1$
$c = 1/2$

$a_n = 1/2 * 2^n$

#### Second Order Linear Homogeneous
*Characteristic Equation* - The most important method
**General Relation Form:**
$a_n = c a_{n-1} +  d a_{n-2}$

**General Solution:**
The general solution of
$a_n = c a_{n-1} +  c a_{n-2}$

Where $r_1$ and $r_2$ are solutions of the characteristic equation, is
If $r_1 \neq r2$
$a_n = c_1 (r_1)^n + c_2 (r_2)^n$
If $r_1 = r_2$
$a_n = c_1r_1^n + c_2nr_1^n$

Where
$r^2 + pr + q = 0$
And $c_1, c_2$ are constants determined by the initial conditions



Steps: Assume $a_n = r^n$, Factor, Roots, General solution, Find constants, Specific solution

**Example:**
$a_n = 2a_{n-1} + 3a_{n-2}$
$a_1 = 1, a_2 = 2$

*1. Assume $a_n = r^n$*

*2. Form characteristic equation*
$r^n = 2(r^{n-1}) + 3(r^{n-2})$ *<-- sub in $r^n$*
$r^2 = 2r + 3$ *<-- divide by $r^{n-2}$*
$r^2 - 2r - 3 = 0$ *<-- rearrange to equal 0 - form quadratic*
$(r + 1)(r - 3)$ *<-- Solve quadratic for roots - by hand or using quadratic formula*
$r = 3$ or $r = -1$

*3. Form general solution*
$a_n = c_1 * 3^n + c_2 * (-1)^n$ *<-- $c_1, c_2 \in \mathbb{R}$, constants*
*Simplify here if able*

*4. Use initial conditions to find the constants*
$a_1 = 1$
$a_1 = c_1 * 3^1 + c_2 * (-1)^1$ 
$1 = 3c_1 - c_2$

$a_2 = 2$
$a_2 = c_1 * 3^2 + c_2 * (-1)^2$ 
$2 = 9c_1 + c_2$

*Add the first equation to the second (or subtract the first from the second, whatever's easier)*
$(9c_1 + c_2) + (3c_1 - c_2) = 2 + 1$
$12c_1 = 3$
$c_1 = 3/12 = 1/4$
*Substitute into first equation*
$1 = 3c_1 - c_2$
$1 = 3/4 + c_2$
$c_2 = -1/4$

*5. Form specific solution*
*Substitute in constants to general formula*
$a_n = c_1 * 3^n + c_2 * (-1)^n$
$c_1 = 1/4$
$c_2 = -1/4$
*Final answer:*
$a_n = 1/4 * 3^n - 1/4 * (-1)^n$


#### Linear Nonhomogeneous
A linear nonhomogenous recurrence is essentially a linear homogeneous relation with a *forcing function* $g(n)$ added that "forces" the sequence away from the homogeneous solution

**General Form:**
$a_n​=c_1​a_{n−1}​+c_2​a_{n−2}​+\dots+g(n)$

To solve these recurrences:
Solve the homogeneous portion of the recurrence
Guess a particular solution based on the forcing term
Add them together to find the general solution of the nonhomogeneous recurrence
Apply the initial conditions


*Step 1: Solve the homogeneous part*
*Step 2: Find a particular solution*
*Step 3: Combine homogeneous and particular solutions*
*Step 4: Use initial condition(s) to find final solutions*


**Finding a particular solution**
First, look at the type of $g(n)$

| $g(n)$                  | Trial Particular Solution |
| ----------------------- | ------------------------- |
| Constant <br>$c$        | $p$                       |
| Linear<br>$c_1 n + c_2$ | $p n + q$                 |
| Exponential <br>$c^n$   | $p * c^n$                 |
Pick the form suggested by the table
Check for overlap with the homogeneous solution
If your trial solution duplicates a term in the homogeneous solution, multiply your trial solution by $n$ until it no longer overlaps

$a_n =$ your particular solution

Then, substitute it into the full recurrence relation
Simplify and solve for the constants, substituting them back into the formula



**Example:**
$a_n = 2a_{n-1} + 3^n$
$a_1 = 1$

*Step 1: Solve the homogeneous part*
$a_n^{(h)} = 2a_{n-1}$
$a_n^{(h)} = C * 2^n$ *General solution for a first-order linear homogeneous relation*

*Step 2: Find a particular solution*
$g(n) = 3^n$
$a_n = p * 3^n$ *Solution for an exponential forcing function*
*Substitute into recurrence*
$[p * 3^n] = 2[p * 3^{n-1}] + 3^n$
*Simplify - divide by $3^{n-1}$*
$3p = 2p + 3$
$p = 3$
So
$a_n^{(p)} = 3 * 3^n$

*Step 3: Combine homogeneous and particular solutions*
$a_n^{(h)} = C * 2^n$
$a_n^{(p)} = 3 * 3^n$

$a_n = a_n^{(h)} + a_n^{(p)}$
$a_n = C * 2^n + 3 * 3^n$

*Step 4: Use initial condition(s)*
$a_n = C * 2^n + 3 * 3^n$
$a_1 = 1$

$1 = C * 2^1 + 3 * 3^1$
$1 = C * 2 + 9$
$C = -8/2$
$C = -4$

$a_n = C * 2^n + 3 * 3^n$
$a_n = -4 * 2^n + 3 * 3^n$


**Example with duplication:**
$a_n = 2a_{n-1} + 2^n$
$a_1 = 1$

*Step 1: Solve homogeneous part*
$a_n^{(h)} = 2a_{n-1}$
$a_n^{(h)} = C * 2^n$

*Step 2: Find a particular solution*
$g(n) = 2^n$
*Trial particular solution from table*
$a_n^{(p)} = D * 2^n$
*This is already in the homogeneous solution, so multiply by $n$*
$a_n^{(p)} = D * n * 2^n$
*Substitute into full recurrence*
$a_n = 2a_{n-1} + 2^n$
$[D * n * 2^n] = [D * (n-1) * 2^{n-1}] + 2^n$
*Simplify - divide both sides by $2^n$*
$Dn = D(n-1) + 1$
$Dn = Dn - D + 1$
$0 = -D + 1$
$D = 1$
*Substitute into particular solution*
$a_n^{(p)} = D * n * 2^n$
$a_n^{(p)} = n * 2^n$

*Step 3: Combine solutions*
$a_n^{(h)} = C * 2^n$
$a_n^{(p)} = n * 2^n$

$a_n = a_n^{(h)} + a_n^{(p)}$
$a_n = C * 2^n + n * 2^n$
$a_n = (C + n)2^n$

*Step 4: Use initial condition(s)*
$a_1 = 1$
$a_n = (C + n)2^n$

*Solve using initial condition(s) to find constant*
$1 = (C+1)2^1$
$C+1 = 1/2$
$C = -1/2$

*Final solution:*
$a_n = (n - 1/2) * 2^n$
