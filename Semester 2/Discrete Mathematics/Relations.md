Let $A$ and $B$ be [[Semester 2/Discrete Mathematics/Sets|sets]]
A *relation* from $A$ to $B$ is a subset of $A \times B$

Define the relation $R$ on sets $A$ and $B$
$R = \{(a, b) \in A \times B | condition\}$

**Example:**
$A = \{1, 2, 3\}$ 
$B=\{4, 5, 6\}$
$R = \{(a, b) \in A \times B | a,b<5\}$
$R = \{(1, 4), (2, 4), (3, 4)\}$


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

Whenever $(a,b)$ and $(b,c)$ exist in $R$, so does $(a,c)$

"$a$ is an ancestor of $b$" is transitive 

### Closures
