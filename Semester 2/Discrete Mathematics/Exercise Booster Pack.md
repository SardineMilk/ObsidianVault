### Sets

### Mathematical Induction
Q1
Use mathematical induction to prove that for any positive integer $n$,
 $1+2+3+...+n = \frac {n(n+1)}{2}$

A1
Let $P(n)$ be the statement 
$1+2+...+n = \frac {n(n+1)}{2}$

$P(1)$ states 
$1 = \frac {1(1+1)}{2} = \frac {1*2}{2} = \frac {2}{2} = 1$
This is true, so $P(1)$ holds

Assume $P(k)$ is true:
$1 + \dots + k = \frac {k(k+1)}{2}$
We need to show that $P(k+1)$ is true:
$1 + \dots + k + (k+1) = \frac {(k+1)(k+1+1)}{2}$
Starting from the left hand side:
$1 + \dots + k + (k+1)$
= $[\frac {k(k+1)}{2}] + (k+1)$
 $= \frac {k(k+1)}{2} + (k+1)$
 $= \frac {k(k+1)}{2} + \frac {2(k+1)}{2}$
 $= \frac {k(k+1)+2(k+1)}{2}$
 $= \frac {(k+1)*(k+2)}{2}$
 This matches the right hand side
 Thus, we see that $P(k+1)$ follows from $P(k)$
 By the principle of mathematical induction, $P(n)$ is true for any positive integer $n$