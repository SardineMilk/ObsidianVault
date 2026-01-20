Mathematical Induction is a [[Proofs|proof]] technique
Used for statements that depend on integers

### How It Works
$P(n)$ is the statement you are trying to prove, a formula 
$n$ is any positive integer, substituted into all $n$ symbols in the formula

To prove $P(n)$, first you prove that $P(1)$ holds (is true).
This is called the **base case**
Sometimes the base case will be 

Then comes the **inductive step**. 
You assume that $P(k)$ is true, with $k$ being any positive integer.
You have to prove that $P(k+1)$ is also true
You do this by refactoring the LHS of $P(k+1)$ to be equivalent to the RHS.
Since you are assuming $P(k)$ holds, you can substitute it into parts of $P(k+1)$ if needed
- The sequences example explains this in practice
This proves that *if* $P(k)$ is true, then $P(k+1)$ *must* be true

How does this prove anything?
You've shown that $P(1)$ holds
You've also shown that if $P(k)$ holds, then $P(k+1)$ also holds
So:
$P(1)$ holds, so $P(1+1)$ -> $P(2)$ holds.
$P(2)$ holds, so $P(3)$ holds
$P(3)$ holds, so...
and so on for every positive integer greater than the base case

### Procedure
Here's a very simple proof by induction, to show how it works
**Step 1:** 
*State $P(n)$*
Let $P(n)$ be the statement $n * 2 = n + n$ 

**Step 2:** Base Case
*Show that $P(1)$ is true*

$P(1)$ states that $1 * 2 = 1 + 1$
This is true, so $P(1)$ holds

**Step 3:** Inductive Step
*Show that if $P(k)$ is true then $P(k+1)$ is true, where $k$ is any positive integer*
Assume $P(k)$ is true: $k * 2 = k + k$
We must show $P(k+1)$ is true:
*refactor $P(k+1)$ so the RHS is equivalent to the LHS*
$(k+1) * 2 = (k + 1) + (k + 1)$
$2k + 2 = k + 1 + k + 1$
$2k + 2 = 2k + 2$
Since $2k + 2 = 2k + 2$ is true, we see that $P(k + 1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$

### Sequences
#### Question
Let $\{s_n\}$ be the sequence defined by
$s_n = 1 + 2 + ... + n$
Guess a formula for $s_n$ and use induction to prove it
#### Answer
*Compute values manually*
1 - 1
2 - 3
3 - 6
4 - 10

*Guess a formula*
$s_n = \frac {n(n+1)}{2}$

*Create statement*
Let $P(n)$ be the statement $1+2+3+...+n = \frac {n(n+1)}{2}$

*Prove base case*
$P(1)$ states states $1 = \frac {1(1+1)}{2}$
- $1 = \frac {1*2}{2}$
- This is true, so $P(1)$ holds

*Inductive step*
Assume $P(k)$ holds for some integer $k$:
$1 + ... + k = \frac {k(k+1)}{2}$
We must show $P(k+1)$ holds:
$1 + ... + k + (k+1) = \frac {(k+1)(k+1+1)}{2}$
*start with left hand side*
$1 + ... + k + (k+1)$
*substitute in $P(k)$ right hand side*
= $[\frac {k(k+1)}{2}] + (k+1)$
*show this is equal to $P(k+1)$ right hand side by refactoring*
 $= \frac {k(k+1)}{2} + (k+1)$
 $= \frac {k(k+1)}{2} + \frac {2(k+1)}{2}$
 $= \frac {k(k+1)+2(k+1)}{2}$
 $= \frac {(k+1)*(k+2)}{2}$
 This matches the right hand side
 Thus, $P(k+1)$ holds
 
 Since $P(k+1)$ follows from $P(k)$,
 By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$

### Divisibility
*Statement*
Let $P(n)$ be the statement $2 | n * (n + 1)$

*Prove base case*
$P(1)$ states 
$2|1*(1+1)$
$2|1*2$
$2|2$
This is true, so $P(1)$ holds

*Inductive step*
Assume $P(k)$ is true: 
$2|k*(k+1)$
*definition of divisibility*
So there exists some integer $m$ such that
$k * (k + 1) = 2m$
We must show $P(k+1)$ is true:
$2|(k+1)*(k+2)$
*refactor, then substitute in the inductive hypothesis*
$= k * (k+1) + 2 * (k+1)$
$= 2m + 2 * (k+1)$
*factor out the divider*
$= 2 (m + (k+1))$

Both $m$ and $k$ are integers, so $m + (k+1)$ is an integer
Since $m + (k+1)$ is an integer,  $(k+1)*(k+2)$ is divisible by 2,
so $P(k+1)$ holds
Thus, we see that $P(k+1)$ follows from $P(k)$
By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$


### Common Problems

#### False Base Case
1.
Let $P(n)$ be the statement $n = n + 1$
2.
$P(1)$ states that $1 = 1 + 1$ 
This is True *Incorrect*
3.
Assume $P(k)$ is true: $k = k + 1$
Then
- $(k + 1) = (k + 1) + 1$
- $k + 1 = k + 2$
So $P(k + 1)$ is true

##### Explanation
It is not enough to prove that is $P(k)$ is true then $P(k + 1$ is true
The base case $P(1)$ must also be true

#### Limited Inductive Step
In the inductive step only prove for some integers, not for any arbitrary integer


### Relevant Exercises
![[Exercises#1.4.1]]

![[Exercises#1.4.2]]

![[Exercises#1.4.3]]

![[Exercises#1.4.4]]

![[Exercises#1.4.5]]