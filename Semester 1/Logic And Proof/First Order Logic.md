#fol
First-order logic is more complicated and complete than [[Propositional Logic]]

> first-order logic = PL + predicates + functions + quantifiers.

[[Logic-book.pdf#page=157&selection=33,0,33,60|Logic-book, page 157]]

**Predicates:** describe the properties of objects
**Functions:** map objects from one to another
**Quantifiers:** allow us to reason about many objects at once

### Predicates
#### Description
Predicates describe the properties of objects (sets)
#### Examples
$Dog(x)$ states that $x$ is a dog
$Fluffy(x)$ states that $x$ is fluffy 
$Loves(x, y)$ states that $x$ loves $y$
 

### Quantifiers
#### Description
Binds a variable and specifies the conditions where the formula should hold

| Symbol    | Description                       | Name        | Code    |
| --------- | --------------------------------- | ----------- | ------- |
| $\exists$ | there exists at least one x where | existential | \exists |
| $\forall$ | for all x this is true            | universal   | \forall |
#### Examples
$\exists x(Dog(x) \land Fluffy(x))$
At least one dog exists that is fluffy

$\forall x (Dog(x) \land Good(x))$
Every dog is good

$\forall x \exists y (Dog(x) \land Person(y) \land Loves(y, x))$
For every dog, there exists a person that loves the dog

There is a person that everyone else loves
$\exists p (Person(p) \implies \forall q. (Person(q) \land q \neq p \implies Loves(q, p)))$

The empty set exists
$\exists S. (Set(S) \land \neg \exists x. x \in S)$

### Aristotelian Forms
Useful patterns for FOL

| Formula                                | Description       |
| -------------------------------------- | ----------------- |
| $\forall x. (A(x) \implies B(x))$      | All As are Bs     |
| $\forall x. (A(x) \implies \neg B(X))$ | No As are Bs      |
| $\exists x. (A(x) \land B(x))$         | Some As are Bs    |
| $\exists x. (A(x) \land \neg B(x))$    | Some As aren't Bs |



### Set background

Uses [[Semester 1/Logic And Proof/Sets]]

Need notation to take order into account

(a, b) - ordered pairs

A, B sets

A x B = {(a, b): a$\in$A, b$\in$B}
product

Example:
A = {a, b, c}, B = {1, 2}

A x B = {(a, 1), (a, 2), (b, 1), (b, 2), (c, 1), (c, 2)}

----
Binary Relations

Relations between two sets

Examples
1.
$x, y, \in N$

x | y means $y = x*Z$ for some $Z \in N$
x times some whole number is y

2 | 4 is true
3 | 4 is false

2.
<=, <, >=, >

3.
$\subset$ 
"Is a subset of" is a binary relation

4.
$\in$
"is an element of"

5.
$\equiv$
"is logically equivalent to"
defined on the set of all wff in pl

----
(a, b)

directed graphs / digraphs

a -> b

----
Example: A = {1, 2, 3, 4, 5}
$\pi \subset A x A$ 
$\pi$ = {(1, 1), (1, 2), (2, 3), (4, 1), (4, 3), (4, 5), (5, 3)}

draw (1) through (5)
draw arrows for each element
i.e. 1 to 1, 4 to 1, 5 to 3

----
Notational Conventions

Subsets of ordinary sets will be denoted by capital latin letters (A, B, X, Y)

Binary relations will be represented by Greek letters


### First Order Logic

[[Structure]]


**Variables**
x, y, z, ... x_1, x_2, x_3

**Names/Constants**
a, b, c, ... a_1, a_2, a_3
- E.g. pick particular famous person out family tree

**1-place predicate symbols**
P(x), R(x), ...
- Interpreted as subsets

**2-place predicate symbols**
P(x, y), R(x, y), ...
- Interpreted as binary relation

**Idea**
(D, individual elements, subsets, binary relations)
- Variables will range over elements of D
- Constants will pick out particular elements of D
- 1-place predicate will be interpreted as subset
- 2-place will be interpreted as binary relations


#### Examples

**Atomic Formula**
- Predicate who's slots are filled with either variables or constants
- Any combination of variables and constants. e.g:

P(x)
P(a)

P(x, y)
P(x, a)
p(b, u)
P(a, b)


**Parse Trees**

ORDER MATTERS

P(x)

| P   |
| --- |
| \|  |
| x   |


P(x, y)

| P   |     |
| --- | --- |
| \|  | \   |
| x   | y   |

P(a, y)

| P   |     |
| --- | --- |
| \|  | \   |
| a   | y   |

----
**Quantification**

$\forall x$
- universal quantifier
- 'For all x'

| $\forall x$ |
| ----------- |
| \|          |
| a           |

$\exists x$
- existential quantifier
- 'There exists at least one x'

| $\exists x$ |
| ----------- |
| \|          |
| a           |


#### Formal Formula

(F1) - All atomic formulae are formulae
(F2) - Let A and B be formulae
- $\neg A$, $A \land B$, $A \implies B$ etc
- You can put any quantifier in front of any formula
	- $(\forall x) A$, $(\exists y) B$
(F3) - All formulae are obtained by applying (F1) and (F2) a finite number of times


**Example**

No meaning yet, just symbols
P(x), Q(x, y) - atomic formulae
$P(x) \land Q(x, y)$

P(a)
$(\forall z) [P(a) \land Q(x, y) \lor P(a)]$


#### Parse Trees
Brackets will be used only to clarify meaning

**Example**

$(\forall z) [(P(x) \implies Q(x)) \land S(x, y)]$
Variables have scope


|     |            | $\forall x$ |     |     |     |     |
| --- | ---------- | ----------- | --- | --- | --- | --- |
|     |            | \|          |     |     |     |     |
|     |            | $\land$     |     |     |     |     |
|     |            | /           | \   |     |     |     |
|     | $\implies$ |             |     | \   |     |     |
|     | /\         |             |     |     | \   |     |
| P   |            | Q           |     |     | S   |     |
| \|  |            | \|          |     |     | /\  |     |
| x   |            | x           |     | x   |     | y   |


**Subtrees**

|     | o   |     |     |     |
| --- | --- | --- | --- | --- |
|     | \|  |     |     |     |
|     | o   |     |     |     |
|     | \|  |     |     |     |
|     | o   |     |     |     |
|     | \|\ |     |     |     |
|     | o   | v   |     |     |
|     |     | \|\ |     |     |
|     |     | o   | o   |     |
|     |     |     | \|\ |     |
|     |     |     | o   | o   |

Subtree determined by vertex v:

| v   |     |     |
| --- | --- | --- |
| \|\ |     |     |
| o   | o   |     |
|     | \|\ |     |
|     | o   | o   |


#### Scope
Given a formula and an occurrence of a quantifier
The scope of that occurrence is the subtree of the parse tree determined by that occurrence

$(\exists x) (F(x) \land G(x)) \implies ((\exists x)F(x) \land (\exists x)G(x))$


|     |             | $\implies$ |             |             |
| --- | ----------- | ---------- | ----------- | ----------- |
|     |             | /\         |             |             |
|     | $\exists x$ |            | $\land$     |             |
|     | \|          |            | /\          |             |
|     | $\land$     |            | $\exists x$ | $\exists x$ |
|     | /\          |            | \|          | \|          |
| F   | G           |            | F           | G           |
| \|  | \|          |            | \|          | \|          |
| x   | x           |            | x           | x           |


#### Bound
An occurrence of variable x is bound if it occurs in scope of occurrence of $\forall x$ or $\exists x$

If an occurrence is not bound it is free

We dont like free variables

A **sentence** or **closed formula** is a formula in which every occurrence of every variable is bound

The idea is that every variable is controlled by a quantifier.
In first order logic, we only study closed formulae


$(\forall x) ((P(x) \implies Q(x)) \land S(x, y))$
all 3 x are under scope of $\forall x$ quantifier, so they are bound
y is not, so it is free


### Connecting Logic with [[Structure]]s

**Idea**
1-place predicate symbol is interpreted as a subset
2-place predicate symbol is interpreted as a binary relation

**Example**
Logic has exactly one 1-place predicate symbol, P [P(x)]
Exactly one 2-place predicate symbol Q, [Q(u, v)]

An interpretation of this logic will consist of the following

(D, A, P)
D - non empty set
A - Interpret P. $A \subset D$
P - Interpret Q. $P \subset D^2$

$A = (\exists x)(P(x) \land Q(x, x))$
This is a sentence
To translate into our structure:

$(\exists x)((x \in A) \land ((x, x) \in P))$
^
$x \in D$

For this to be true, 
we need $d \in D$ such that $d \in A$ and $(d, d) \in P$


**Example 2**
Suppose our logic has exactly one 2-place predicate symbol F(x, y)

Interpretations:
1.
D = all people
Interpret F(x, y) as 'x is the father of y'

2.
D = $N$ = {0, 1, 2, ...}
Interpret F(x, y) as 'x is <= y'

3.
D = $N$ = {0, 1, 2}
Interpret F(x, y) as 'x is > y'

**Example 3**
$(\forall y) (\exists x) F(x, y)$
This is a sentence

1.
D = all people
F(x, y) is interpreted as 'x is the father of y'
For every person y, there is at least one person x that is their father.

2.
D = {0, 1, 2, ...}
F(x, y) is interpreted as 'x <= y'
For every number y, there is a number x that is <= to it
This is true because (n <= n)

3.
D = {0, 1, 2, ...}
F(x, y) is interpreted as 'x < y'
For every number y there is a number x that is < to it
This is false in this structure because there is nothing strictly smaller than 0 in D

----
Once an interpretation is chosen, a sentence S makes an assertion about that structure 

If S is true under that interpretation, we say that interpretation is a *model of S*

If our sentence is true under all interpretations, we say S is *universally valid* or *logically valid*

$\vdash S$ means S is universally/logically valid

If it is not the case that $\vdash S$, there must be a structure in which the interpretation of S is false
This is called a [[Counterexample]]


## Examples
C(X) - x loves comic books
H(x) - x loves history
F(x, y) - x is a friend of y  
W(x, y) - x works with y

a - Phil
b - Pierre

1 
Pierre loves history and Phil loves comic books
$H(a) \land C(b)$ 

2
Someone loves history and comic books
$\exists x. (H(x) \land C(x))$

3 
Phil works with someone who is a friend of someone who loves history
$\exists x \exists y (W(a, x) \land F(x, y) \land H(y))$

4
Everyone works with someone who loves comic books
$\forall x \exists y (W(x, y), C(y))$

5
No one who loves comic books is a friend of someone who doesn't love history
$\forall x \forall y(\neg F(x, y) \land \neg H(Y))$ X
$\forall x (C(x) \implies \forall y (\neg H(y) \implies \neg F(x, y)))$


6
The person Pierre works with who loves history also loves comic books

7
Phil is a friend of at most two people who love history

8 
Pierre works with at least two people who love comic books, but he isn't friends with any of them