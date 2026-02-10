### Definition
Let $A$ and $B$ be [[Semester 2/Discrete Mathematics/Sets|sets]]
A *relation* from $A$ to $B$ is a subset of $A \times B$

Define the relation $R$ on sets $A$ and $B$
$R = \{(a, b) \in A \times B | condition\}$

**Example:**
$A = \{1, 2, 3\}$ 
$B=\{4, 5, 6\}$
$R = \{(a, b) \in A \times B | a,b<5\}$
$R = \{(1, 4), (2, 4), (3, 4)\}$

If $(a, b)$ is in $R$, we can say $a R b$

Relations can be represented by a directed graph of nodes and arrows
$R$ is a relation on $S$:
- Each element $s$ of $S$ is a node in the graph
- Each pair $(a, b)$ in $R$ is an arrow linking element $a$ to $b$ 

### Properties
#### Reflexive
$\forall a \in A, (a, a) \in R$
$R$ contains at least $(a, a)$ for every element $a$ in $A$

"$a$ is the same age as $b$" is reflexive

![[reflexive_relation.png]]

**Example**
$A = \{1, 2, 3\}$
$R = \{(1,1), (2,2), (3,3)\}$ *<- reflexive*
$R = \{(1,1), (2,2), (3,3), (1,2), (2,3)\}$ *<- also reflexive - reflexive does not forbid extra pairs*
$R = \{(1,1), (2,2)\}$ *<- not reflexive: (3,3) is missing*
$R = \{(1,1), (2,2), (1,2), (2, 1)\}$ *<- also not reflexive: extra elements don't fix missing reflexive pairs*

#### Symmetric
$\forall a,b \in A, (a,b) \in R \implies (b,a) \in R$
Whenever $(a,b)$ exists in $R$, $(b,a)$ must also exist

"$a$ is a friend of $b$" is (hopefully) symmetric

![[symmetric_relation.png]]

**Example:**
$A = \{1, 2, 3\}$
$R = \{(1, 3), (3, 1)\}$ *<- symmetric*
$R = \{(1, 3), (3, 1), (1,1), (2,2)\}$ *<- also symmetric*
$R = \{(1, 3), (2, 1)\}$ *<- not symmetric*
$R = \{(3,1), (1,3), (2,1), (2,2), (1,1)\}$ *<- not symmetric - (2, 1) exists by (1, 2) doesn't*

#### Antisymmetric
$\forall a,b \in A, [(a,b) \in R \land (b,a) \in R] \implies [a=b]$
If $(a, b) \in R$ then either $(b, a) \notin R$ or $a = b$

"$a$ is the same age or older than $b$" is antisymmetric

The graph never contains a pair of opposite directed edges between two different vertices:
![[antisymmetric_relation.png]]

**Example:**
$A = \{1,2,3\}$
$R = \{(1, 3), (2, 1)\}$ *<- antisymmetric*
$R = \{(1, 3), (2, 1), (1,1),(2,2)\}$ *<- also antisymmetric*
$R = \{(1, 3), (3, 1)\}$ *<- not antisymmetric*
$R = \{(1, 3), (3, 1), (1,1),(2,2)\}$ *<- also not antisymmetric*

**Note:**
*Symmetric* and *antisymmetric* are not opposites
A relation can have both properties, one or neither

$A = \{a, b, c, d\}$
$R = \{(a, a), (b, b), (c, c), (d, d)\}$ is both *symmetric* and *antisymmetric*
$R = \{(a, b), (b, a), (c, d)\}$ is neither *symmetric* nor *antisymmetric* 

#### Transitive
$\forall a,b,c \in A, [(a,b) \in R \land (b,c) \in R] \implies (a,c) \in R$
Whenever $(a,b)$ and $(b,c)$ exist in $R$, so does $(a,c)$

"$a$ is the ancestor of $b$" is transitive 
"$a$ is taller than $b$" is transitive
- If Amy is taller than Bob, and Bob is taller than Charlie, then Amy must be taller than Charlie

![[transitive_relation.png]]

**Example:**
$A = \{1, 2, 3, 4\}$
$R = \{(1, 2), (2, 3), (1, 3)\}$ *<- transitive*
$R = \{(1, 2), (2, 3), (1, 3), (3, 4)\}$ *<- also transitive*
$R = \{(1, 2), (2, 1), (1, 1)\}$ *<- also transitive*
$R = \{(1, 2), (2, 1)\}$ *<- not transitive*
$R = \{(1, 2), (3, 4), (1, 3)\}$ *<- not transitive*


### Equivalence Relations
A relation that is *reflexive*, *symmetric*, and *transitive* is called an *equivalence relation*

**Example:**
$A = \{1, 3, 5, 9, 11, 18\}$
$R = \{(a, b)  \in A \times A | (a - b) \space is \space divisible \space by \space 4\}$

$R = \{​(1,1),(1,5),(1,9),(5,1),(5,5),(5,9),(9,1),(9,5),(9,9),(3,3),(3,11),(11,3),(11,11),(18,18)\}$​
*Reflexive:* $a - a = 0$, so $(a, a)$ must be in $R$
*Symmetric:* if $a - b$ is divisible by 4, so is $b - a$ 
*Transitive:* if $a - b$ and $b - c$ are divisible by 4, so is $a - c$, because $a-c=(a-b)+(b-c)$
Therefore, $R$ is an equivalence relation

#### Equivalence Classes
$R$ is an equivalence relation on $A$
For each element $a$ in $A$, the *equivalence class* of $a$ is the set of all elements $x$ in $A$ where $x$ is related to $a$ by $R$
This is written as $[a]$

$[a] = \{x \in A | (x, a) \in R\}$
because equivalence relations are symmetric:
$\{x \in A | (x, a) \in R\} = \{x \in A | (a, x) \in R\}$
It doesn't matter which way around you do it, you're just looking for any $x$ that is related to $a$

Equivalence classes are *sets*, not relations

**Example:**
$A = \{1, 3, 5, 9, 11, 18\}$
$R = \{​(1,1),(1,5),(1,9),(5,1),(5,5),(5,9),(9,1),(9,5),(9,9),(3,3),(3,11),(11,3),(11,11),(18,18)\}$​

$[1] = \{1, 5, 9\}$ *The set of all elements x where (x, 1) or (1, x) is in R - if one is then both will be*
$[3] = \{3, 11\}$
$[5] = \{1, 5, 9\}$
$[9] = \{1, 5,9\}$
$[11] = \{3, 11\}$
$[18] = \{18\}$

Note that some of the equivalence classes contain the same elements as each other: they're *identical*
Equivalence classes are either *identical* or *completely disjoint* - they never partially overlap
We mostly just care about the *disjoint* or *distinct* equivalence classes.

You can remove any duplicate classes, leaving only one of each element of $A$:
$C_1 = \{1, 5, 9\}$
$C_2 = \{3, 11\}$
$C_3 = \{18\}$

Important properties:
- Every element of $A$ is in *exactly one* class
- Classes *do not overlap*
- Classes added together make $A$

If you drew the graph of a relation, the equivalence classes would be the groups of elements:
![[equivalence-relation.png]]
### Closures
Let $R$ be a relation on set $A$
Take a property: reflexive, symmetric, antisymmetric, transitive

The property closure of $R$ is the *smallest* relation on $A$ that:
- Contains $R$, and
- Has the given property

This is written as:
- $R_r$ for the reflexive closure
- $R_s$ for the symmetric closure
- etc

"Smallest" means adding as few ordered pairs as possible while ensuring the property holds
- exactly what is missing, and no more

A closure of $R$ *always* contains $R$, so:
A closure of $R$ is *never* smaller than $R$

If $R$ already has the property, then $R_{property} = R$

**Example:**
$A = \{1, 2, 3\}$
$R = \{(1,1), (1,2), (2,3)\}$  *<- $R$ is not reflexive*
Find the *reflexive* closure of $R$, referred to as $R_r$:
$R_r = \{(1,1), (1,2), (2,2), (2,3), (3,3)\}$ *<- $R_r$ is reflexive*

$A = \{1, 2, 3\}$
$R = \{(1,1), (1,2), (2,3)\}$  *<- $R$ is not symmetric*
Find the *symmetric* closure of $R$, referred to as $R_s$:
$R_s = \{(1,1), (1,2), (2, 1), (2,3), (3, 2)\}$ *<- $R_s$ is symmetric*

$A = \{1, 2, 3\}$
$R = \{(1,2), (2,3)\}$  *<- $R$ is not transitive*
Find the *transitive* closure of $R$, referred to as $R_t$:
$R_t = \{(1,2), (2,3), (1,3\}$  *<- $R$ is transitive*

$A = \{1, 2, 3\}$
$R = \{(1,1), (1, 2), (2,2), (3,3)\}$  *<- $R$ is reflexive*
Find the *reflexive* closure of $R$, referred to as $R_r$:
$R_r = \{(1,1), (1,2), (2,2), (3,3)\}$  *<- $R_r$ is reflexive*
Because $R$ is already reflexive, $R_r = R$ 
$R$ is not the shortest possible reflexive relation on $A$, but $R_r$ must contain $R$, not just be reflexive.


### Exercises
![[Exercises#1.5.1]]

![[Exercises#1.5.2]]

![[Exercises#1.5.3]]
