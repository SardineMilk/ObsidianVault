Is a [[Proofs|proof]] technique
Used for statements that depend on integers

### Procedure
$P(n)$ is the statement you are trying to prove

**Step 1:** 
State $P(n)$
- Let $P(n)$ be the statement $n * 2 = n + n$ 

**Step 2:** Base Case
Show that $P(1)$ is true
- $P(1)$ states that $1 * 2 = 1 + 1$

**Step 3:** Inductive Step
Show that if $P(k)$ is true then $P(k+1)$ is true, where $k$ is any positive integer 
- Assume $P(k)$ is true: $k * 2 = k + k$
- We must show $P(k+1)$ is true:
	- $(k+1) * 2 = (k + 1) + (k + 1)$
	- $2k + 2 = k + 1 + k + 1$
	- $2k + 2 = 2k + 2$
- Since $2k + 2 = 2k + 2$ is true, we see that $P(k + 1)$ follows from $P(k)$
- By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$

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
Assume $P(k)$ is true:
$1 + ... + k = \frac {k(k+1)}{2}$
We must show $P(k+1)$ is true:
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
 Thus, we see that $P(k+1)$ follows from $P(k)$
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
#### No Inductive Step
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


### Example
Find a formula for sum of the first $n$ odd integers

Let $P(n)$ be the statement 
$1+3+5+7+ ... + (2n - 1) = n^2$

##### Proof:

### Relevant Exercises
![[Exercises#1.4.1]]

![[Exercises#1.4.2]]

![[Exercises#1.4.3]]

![[Exercises#1.4.4]]

![[Exercises#1.4.5]]