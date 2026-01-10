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
- Then 
	- $(k+1) * 2 = (k + 1) + (k + 1)$
	- $2k + 2 = k + 1 + k + 1$
	- $2k + 2 = 2k + 2$
- Since $2k + 2 = 2k + 2$ is true, we see that $P(k + 1)$ follows from $P(k)$
- By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$

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


