We can use these for [[Propositional Logic]]:
It's not required, but we'll use it to train for [[First Order Logic]]

**Example**
Determine when $A = \neg p \implies (q \land r)$
We could use a truth table, but we shall adopt a different approach
We shall work backwards

This has the shape of $x \implies y$
where $x = \neg p$ and $y = q \land r$


| x   | y   | x -> y |
| --- | --- | ------ |
| T   | T   | T      |
| T   | F   | F      |
| F   | T   | T      |
| F   | F   | T      |
$x \implies y$ is true precisely when x is false or y is true

$\neg (\neg p)$ is true (precisely when p is true)
or
$q \land r$ is true (precisely when q and r are true)

#### Truth Table Algorithm
- We shall not use $\oplus ,\top ,\bot$
- We shall use trees as out data structure, but different from Parse [[Parse Trees]]
- Always work backwards

**Example 1**
$A = X \land Y$
"shape"
For example, $(p \implies q) \land (q \implies p)$
$X = p \implies q$,    $Y = q \implies p$
When is $X \land Y$ true?

precisely when X is true and Y is true

$\alpha$ Rule

| $X \land Y$ |     | $X \land Y$ |
| ----------- | --- | ----------- |
| \|          | OR  | \|          |
| X, Y        |     | X           |
|             |     | Y           |

**Example 2**
$A = X \lor Y$

$X \lor Y$ is true precisely when X is true or Y is true or both

$\beta$ Rule

|     | $X \lor Y$  |     |
| --- | ----------- | --- |
|     | /         \ |     |
| X   |             | Y   |


**Rules**
These 2 examples illustrate the 2 rules we shall use in constructing truth trees

Possible shapes:
$X \land Y, X \lor Y, X \implies Y, X \iff Y$
$\neg (X \land Y), \neg (X \lor Y), \neg (X \implies Y), \neg (X \iff Y)$

The shape of a wff is the last or centre-most connective

#### Examples
1.
The truth tree for X and Y is 

| $X \land Y$ |
| ----------- |
| \|          |
| X, Y        |
Look at the bottom row - this is the answer
For $X \land Y$ to be true, you must have true: (X, Y)

2.

|     | $X \lor Y$ |     |
| --- | ---------- | --- |
|     | /        \ |     |
| X   |            | Y   |

You must have true: (X) or (Y)

**Construct truth tree**

1.
$(\neg p) \implies (q \land r)$


|                 | $(\neg p) \implies (q \land r)$  |             |
| --------------- | -------------------------------- | ----------- |
|                 | /                              \ |             |
| $\neg (\neg p)$ |                                  | $q \land r$ |
| \|              |                                  | \|          |
| $p$             |                                  | $q, r$      |
$(p) \lor (q \land r)$


2.
$A = (p \lor q) \implies (p \land q)$

|                   | $(p \lor q) \implies (p \land q)$    |                |
| ----------------- | ------------------------------------ | -------------- |
|                   | /                                  \ |                |
| $\neg (p \lor q)$ |                                      | $( p \land q)$ |
| \|                |                                      | \|             |
| $\neg p, \neg q$  |                                      | $p, q$         |
$A \equiv(\neg p \land \neg q) \lor (p \land q)$

#### Truth Trees for each shape

We shall draw them using the following logical equivalences

- $X \implies Y \equiv \neg X \lor Y$
- $\neg (X \land Y) \equiv \neg X \lor \neg Y$
- $\neg (X \lor Y) \equiv \neg X \land \neg Y$
- $\neg \neg X \equiv X$
- $\neg (X \iff Y) \equiv X \oplus Y$

9 Shapes in total

#### $X \land Y$

| $X \land Y$ |
| ----------- |
| \|          |
| X, Y        |


#### $X \lor Y$
|     | $X \land Y$ |     |
| --- | ----------- | --- |
|     | /         \ |     |
| $X$ |             | $Y$ |

#### $X \implies Y$

|          | $X \implies Y$     |     |
| -------- | ------------------ | --- |
|          | /                \ |     |
| $\neg X$ |                    | Y   |

#### $X \iff Y$
|        | $X \iff Y$         |                  |
| ------ | ------------------ | ---------------- |
|        | /                \ |                  |
| $X, Y$ |                    | $\neg X, \neg Y$ |

----
#### $\neg \neg X$

| $\neg \neg X$ |
| ------------- |
| \|            |
| X             |

----
#### $\neg (X \land Y)$
|          | $\neg (X \land Y)$ |          |
| -------- | ------------------ | -------- |
|          | /                \ |          |
| $\neg X$ |                    | $\neg Y$ |

#### $\neg (X \lor Y)$

| $\neg (X \lor Y)$ |
| ----------------- |
| \|                |
| $\neg X, \neg Y$  |

#### $\neg (X \implies Y)$
| $\neg (X \implies Y)$ |
| --------------------- |
| \|                    |
| $X, \neg Y$           |

#### $\neg (X \iff Y)$

|             | $\neg (X \implies Y)$ |             |
| ----------- | --------------------- | ----------- |
|             | /                \    |             |
| $\neg X, Y$ |                       | $X, \neg Y$ |


#### Terminology
- Truth flows down the branches
- $\lor$ is used between branches
- $\land$ for all literals on a branch
- if a tick is beside a wff, we say that wff has been used 
- If a branch contains X and $\neg$X, we say that branch is closed and mark it with a cross
- The algorithm only applies to non closed branches
- If all branches are closed, the formula is a contradiction

**Important Example**
$\neg ((p \lor q) \implies (p \land q))$
$p

|               | $\neg ((p \lor q) \implies (p \land q))$<br> |               |
| ------------- | -------------------------------------------- | ------------- |
|               | \|                                           |               |
|               | $(p \lor q)$, $\neg (p \land q)$             |               |
|               | /                     \                      |               |
| $p$, $\neg p$ |                                              | $q$, $\neg q$ |
| X             |                                              | X             |
^ this is wrong


**Extra example**

|                            | $(p \land (q \implies r)) \lor (\neg p \land (r \implies q))$ |                                 |
| -------------------------- | ------------------------------------------------------------- | ------------------------------- |
|                            | /                                                  \          |                                 |
| $(p \land (q \implies r))$ |                                                               | $(\neg p \land (r \implies q))$ |
| \|                         |                                                               | \|                              |
| $p$, $q \implies r$<br>    |                                                               | $\neg p$, $r \implies q$        |
| / \                        |                                                               | /          \                    |
| $\neg q$, $r$              |                                                               | $\neg r$, $q$                   |
$(\neg q \land p) \lor (r \land p) \lor (\neg p \land \neg r) \lor (\neg p \land q)$


### Using Truth Trees

- To show that a wff is satisfiable, show that its completed truth tree has at least one open branch.

**Example**
Show that $A = \neg ((p \lor q) \implies (p \land q))$


|          |          | A                  |          |          |
| -------- | -------- | ------------------ | -------- | -------- |
|          |          | \|                 |          |          |
|          |          | $p \lor q$         |          |          |
|          |          | $\neg (p \land q)$ |          |          |
|          |          | /          \       |          |          |
|          | $p$      |                    | $q$      |          |
|          | /    \   |                    | /      \ |          |
| $\neg p$ | $\neg q$ |                    | $\neg p$ | $\neg q$ |
| x        | o        |                    | o        | x        |
This completed truth tree has an open branch, therefore A is satisfiable

$p \lor q$ leads to p and q
$\neg (p \land q)$ leads to $\neg p$ and $\neg q$
Add to both branches
Cancel out $\neg$ and normal


#### Disjunctive Normal Form

To convert a completed truth tree into [[Functional Completeness| Disjunctive Normal Form]], use all the open branches.
$(p \land \neg q) \lor (\neg p \land q$)$


#### Tautology and Contradiction

To show that X is a contradiction, show that a truth-tree for X has every branch closed

To show that X is a tautology, show that $\neg X$ is a contradiction



To show that $A \equiv B$ using truth trees,
$A \equiv B$ precisely when $\vdash A \iff B$

We must place at the root of the tree $\neg (A \iff B)$
And show that every branch is closed

--- 
The argument $A_1,...A_n \therefore B$ is valid precisely when
$\vdash (A_1 \land ... \land A_n) \implies B$

When $\neg((A_1 \land ... \land A_n) \implies B)$  is a contradiction

$X \implies Y \equiv  \neg X \lor Y$
$\neg(\neg (A_1 \land ... \land A_n) \lor B)$ 
$\neg \neg (A_1 \land ... \land A_n) \land \neg B$ 
$(A_1 \land ... \land A_n) \land \neg B$ 
$A_1 \land ... \land A_n \land \neg B$ 


|     | $A_1$    |
| --- | -------- |
|     | .        |
|     | .        |
|     | .        |
|     | $A_n$    |
|     | $\neg B$ |
|     | \|       |
|     |          |
Check the completed truth tree has every branch closed

**Example**
Show the argument $p \implies q, r \implies q, p \lor r \therefore q$

|     |          | $p \implies q$ | (1) |
| --- | -------- | -------------- | --- |
|     |          | $r \implies q$ | (3) |
|     |          | $p \lor r$     | (2) |
|     |          | $\neg q$       |     |
|     |          | /   \          |     |
|     | $\neg p$ |                | $q$ |
|     | /    \   |                | x   |
| p   |          | r              |     |
| x   |          | / \            |     |
|     | $\neg r$ | p              |     |
|     | x        | x              |     |
Because every branch in the completed truth tree is closed, the argument is valid

----
## For [[First Order Logic]]

Input S (sentence)

Question: Is S (universally/logically) valid
$\vdash S$

Start the truth tree $\neg S$ 
If the truth tree closes then $\vdash S$

**Quantifiers**
If X and Y are sentences
We write that $X \equiv Y$ if X and Y have the same truth value in each structure

**De Morgan's law for Quantifiers**
$\neg (\forall x) A \equiv (\exists x) \neg A$

**Existential Quantifiers**
$(\exists x) ((x^2=2) \land (x \in R) \land (x >= 0))$

We give a name to the real number that has these properties
sqrt(2)
This get rids of an existential quantifier
All we need to remember is the properties this has

*This idea can be generalised:*
Let A be any formula
A[x] means that x occurs free in A
if a is any constant then
A[a] means replace all free occurrences of x by a

Given $(\exists x) A[x]$
Give a name (e.g. a) to the element that exists and has these properties.
This a is an element so that $A[a]$

We have to be careful
We cannot use any constant we have used before


### FOL Truth Tree Rules

All truth tree rules for PL still apply

$\neg (\forall x) A$ 
|
$(\exists x) \neg A$

$\neg (\exists x) A$ 
|
$(\forall x) \neg A$

**New Name Rule**
$(\exists x) X[x]$ (1)
|
$X[a]$

Where we add $X[a]$ at the bottom of all branches containing (1), and a is a constant that does not already occur in the branch containing a 

**Never Ending Rule**

$(\forall x) X[x]$
|
$X[a]$

Where we add $X[a]$ at the bottom of any branch containing (2) and a is *any* constant appearing in the branch containing (2) OR a is a new constant if no new constants have yet been introduced


#### Be aware:
- Order matters
- Strategically apply the new name rule before the never-ending rule

To show that $\vdash A$ is valid, show that *some* truth tree with $\neg A$ at it's root closes

TO prove $A_1, ..., A_n \therefore B$
is a valid argument show that *some* truth tree beginning at the root closes
### Examples

**Example:**
$A[x] = B[x] \land (\exists x) C(x)$
replace all free occurrences
$A[x] = B[a] \land (\exists x) C(x)$


