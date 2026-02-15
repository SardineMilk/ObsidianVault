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


**Example:**
$a_n = 2a_{n-1} + 3^n$
$a_1 = 1$

*Step 1: Solve the homogeneous part*
$a_n^{(h)} = 2a_{n-1}$
$a_n^{(h)} = C * 2^n$ *General solution for a first-order linear homogeneous relation*

*Step 2: Find a particular solution*
$g(n) = 3^n$
$a_n = p * 3^n$ *Solution for an exponential forcing function from the table*
*Substitute into recurrence*
$[p * 3^n] = 2[p * 3^{n-1}] + 3^n$
*divide by $3^{n-1}$*
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
