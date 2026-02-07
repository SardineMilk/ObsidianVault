Probability theory provides *mathematical models* for understanding *random experiments* 

A probability model has two components:
- *sample space*
- *probability function*

### Sample Space
The set of all possible outcomes of a random experiment
Labelled as $S$

This course will only deal with *discrete* sample spaces: non-continuous
Example non-discrete: Throw a dart at graph paper, real number coordinates

Any subset of a sample space is called an *event*

**Example**
Rolling a die once:
$S = \{1,2,3,4,5,6\}$ *<- sample space*
$A = \{2, 4, 6\}$ *<- event that the outcome is even*
$B = \{1, 2, 3\}$*<- event that the outcome is less than 4*

**Example:**
Construct a sample space for flipping a coin twice and getting heads exactly once
$S = \{TT, TH, HT, HH\}$
$A = \{TH, HT\}$

### Probability Function
$P(E)$ assigns a value between $0$ and $1$ to and event $E \subset S$
This value is the *probability* of event $E$

For all subsets $E$ of $S$, $0 \leq P(E) \leq 1$
$P(\emptyset) = 0$
$P(S) = 1$

For disjoint sets:
$A,B \subset S, A \cap B = \emptyset$ *<- disjoint sets*
$P(A \cup B) = P(A) + P(B)$
$P(E_1 \cup E_2 \cup \dots \cup E_n) = P(E_1) + P(E_2) + \dots + P(E_n)$

For any arbitrary sets:
$A, B \subset S$
$P(A \cup B) = P(A) + P(B) - P(A \cap B)$

**Example: disjoint sets**
Roll a 6 sided die
$S = \{1,2,3,4,5,6\}$
$P(1) = \frac{1}{6}$
$P(3) = \frac{1}{6}$
$P(5) = \frac{1}{6}$
$P(rolling \space odd \space number) = \frac{3}{6}$


### Conditional and Independent Probability

#### Conditional

A fair coin is tossed twice 
The coin landed heads up at least one time. (Event $A$)
We are told the coin didn't land heads up both times

What is the probability?

| $P(E)     | 1/4 | 1/4 | 1/4 | 1/4 |
| --------- | --- | --- | --- | --- |
| E         | hh  | ht  | th  | tt  |
| $P(E\|A)$ | 1/3 | 1/3 | 1/3 | 0   |

We define P(E|A) as *conditional* probability
E happening subject to A already having occurred

Observe: 1/4 = 3/4 * 1/3
$P(E|A) = P(E) / P(A)$
Here, E is a simple/elementary outcome

In general:
$P(A|B) = \frac {P(B \cap A)}{P(A)}$

##### Example 2.12
A fair coin is tossed 3 times
What is the probability that the first toss was tails: $B$
Given that at least one toss was heads: $A$

$S = \{TTT, TTH, THT, THH, HTT, HTH, HHT, HHH\}$
$A = 7/8$
$B = 4/8$
$A \cap B = 3/8$
$A|B = \frac {P(A \cap B)}{P(A)}$
$A|B = \frac{3/8}{7/8}$
$A|B = \frac{3}{7}$

##### Example 2.13
An urn contains 6 red balls and 3 blue balls
The balls are drawn one at a time

What is the probability that the first ball is red: $A$

All ways to draw 3 balls = 
$\binom{9}{3} = \frac {9!}{(9-3)!} = 9 * 8 * 7$

### Independent
A fair coin is tossed twice
The events of the first and second toss are *independent*



$P(A|B) = P(A)$
and 
$P(B|A) = P(B)$


#### Equiprobable
If two events have the same probability, they are *equiprobable*

X and Y roll a die
If the outcome is prime, X wins, else Y wins

Roll a die :$\{1,2,3,4,5,6\}$
Primes on a die: $\{2,3,5\}$
$P(prime) = \frac{3}{6} = \frac{1}{2}$
$P(not \space prime) = \frac{3}{6} = \frac{1}{2}$
