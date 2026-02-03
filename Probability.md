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



16 * 30 = 480

100/480
100/479
...
100/380

480
100

= 
480! / (480-100)! * 100!