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

### Properties
#### Reflexive
$\forall a \in A, (a, a) \in R$
$R$ contains at least $(a, a)$ for every element $a$ in $A$

"$a$ is the same age as $b$" is reflexive

**Example**
$A = \{1, 2, 3\}$
$R = \{(1,1), (2,2), (3,3)\}$ *<- reflexive*
$R = \{(1,1), (2,2), (3,3), (1,2), (2,3)\}$ *<- also reflexive*
$R = \{(1,1), (2,2)\}$ *<- not reflexive*
$R = \{(1,1), (2,2), (1,2), (2, 1)\}$ *<- also not reflexive*

#### Symmetric
$\forall a,b \in A, (a,b) \in R \implies (b,a) \in R$
Whenever $(a,b)$ exists in $R$, $(b,a)$ must also exist

"$a$ is a friend of $b$" is (hopefully) symmetric

**Example:**
$A = \{1, 2, 3\}$
$R = \{(1, 3), (3, 1)\}$ *<- symmetric*
$R = \{(1, 3), (3, 1), (1,1), (2,2)\}$ *<- also symmetric*
$R = \{(1, 3), (2, 1)\}$ *<- not symmetric*
$R = \{(3,1), (1,3), (2,1), (2,2), (1,1)\}$ *<- not symmetric*


#### Antisymmetric
$\forall a,b \in A, [(a,b) \in R \land (b,a) \in R] \implies [a=b]$
The only way both $(a,b)$ and $(b,a)$ are in $R$ is when $a=b$

"$a$ is the same age or older than $b$" is antisymmetric

**Example:**
$A = \{1,2,3\}$
$R = \{(1, 3), (2, 1)\}$ *<- antisymmetric*
$R = \{(1, 3), (2, 1), (1,1),(2,2)\}$ *<- also antisymmetric*
$R = \{(1, 3), (3, 1)\}$ *<- not antisymmetric*
$R = \{(1, 3), (3, 1), (1,1),(2,2)\}$ *<- also not antisymmetric*


#### Transitive
$\forall a,b,c \in A, [(a,b) \in R \land (b,c) \in R] \implies (a,c) \in R$
Whenever $(a,b)$ and $(b,c)$ exist in $R$, so does $(a,c)$

"$a$ is the ancestor of $b$" is transitive 
"$a$ is taller than $b$" is transitive
- If Amy is taller than Bob, and Bob is taller than Charlie, then Amy must be taller than Charlie

**Example:**
$A = \{1, 2, 3, 4\}$
$R = \{(1, 2), (2, 3), (1, 3)\}$ *<- transitive*
$R = \{(1, 3), (3, 4), (1, 4)\}$ *<- also transitive*
$R = \{(1, 2), (2, 3), (1, 3), (3, 4)\}$ *<- also transitive*
$R = \{(1, 2), (3, 4), (1, 3)\}$ *<- not transitive*

#### Equivalence Relations
A relation that is *reflexive*, *symmetric*, and *transitive* is called an *equivalence relation*

**Example:**
$A = \{1, 3, 5, 9, 11, 18\}$
$R = \{(a, b)  \in A \times A | a \equiv b (mod 4)\}$
$R = \{​(1,1),(1,5),(1,9),(5,1),(5,5),(5,9),(9,1),(9,5),(9,9),(3,3),(3,11),(11,3),(11,11),(18,18)\}$​
*Reflexive:* $a - a = 0$, so $(a, a)$ must be in $R$
*Symmetric:* if $a - b$ is divisible by 4, so is $b - a$
*Transitive:* if $a - b$ and $b - c$ are divisible by 4, so is $a - c$
Therefore, $R$ is an equivalence relation

##### Equivalence Classes
$R$ is an equivalence relation on $A$
For each element $a$ in $A$, the *equivalence class of $a$* is the set of all elements $x$ in $A$ where $x$ is related to $a$ by $R$
This is written as $[a]$

$[a] = \{x \in A | (x, a) \in R\}$

**Example:**
$A = \{1, 3, 5, 9, 11, 18\}$
$R = \{​(1,1),(1,5),(1,9),(5,1),(5,5),(5,9),(9,1),(9,5),(9,9),(3,3),(3,11),(11,3),(11,11),(18,18)\}$​

$[1] = \{1, 5, 9\}$ *The set of all elements x where (x, 1) or (1, x) is in R - if one is both will be*
$[3] = \{3, 11\}$
$[5] = \{1, 5, 9\}$
$[9] = \{1, 5,9\}$
$[11] = \{3, 11\}$
$[18] = \{18\}$

Note that some of the equivalence classes contain the same elements as each other
We mostly just care about the *disjoint* or *distinct* equivalence classes.
You can remove any duplicate classes, leaving only one of each element of $A$:
$C_1 = \{1, 5, 9\}$
$C_2 = \{3, 11\}$
$C_3 = \{18\}$


### Closures
