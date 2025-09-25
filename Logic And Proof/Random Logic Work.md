#work 

Put $A = \neg(p \implies (q \lor (p \land r)))$

Construct parse tree of A
![[randomlogictree]]

Construct Truth Table of A


| p   | q   | r   | $p \land r$ | $\lor q$ | $p \implies$ | A   |
| --- | --- | --- | ----------- | -------- | ------------ | --- |
| T   | T   | T   | T           | T        | T            | F   |
| T   | T   | F   | F           | T        | T            | F   |
| T   | F   | T   | T           | T        | T            | F   |
| T   | F   | F   | F           | F        | F            | T   |
| F   | T   | T   | F           | T        | T            | F   |
| F   | T   | F   | F           | T        | T            | F   |
| F   | F   | T   | F           | F        | T            | F   |
| F   | F   | F   | F           | F        | T            | F   |

Write in Disjunctive Normal Form
$A \equiv (p \land \neg q \land \neg r)$


2. Write $p \implies q$ using p, q, nand only

| p   | q   | $\implies$ |
| --- | --- | ---------- |
| T   | T   | T          |
| T   | F   | F          |
| F   | T   | T          |
| F   | F   | T          |

| p   | $\neg q$ | nand |
| --- | -------- | ---- |
| T   | F        | T    |
| T   | T        | F    |
| F   | F        | T    |
| F   | T        | T    |
p nand (q nand q)

p nand q $\equiv \neg (p \land q)$
$p \implies q \equiv \neg p \lor q$

De Morgan
p nand q $\equiv \neg p \lor \neg q$
p nand (q nand q) $\equiv p \lor \neg q$



**Example**

using $\neg, \implies$

| p   | q   | $p \iff q$ |
| --- | --- | ---------- |
| T   | T   | T          |
| T   | F   | F          |
| F   | T   | F          |
| F   | F   | T          |
