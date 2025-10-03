#### For [[Propositional Logic]]:
- not required, but we'll use it to train for [[First-Order Logic]]

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
