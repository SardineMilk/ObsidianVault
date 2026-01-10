#pl

When comparing formulae, use $\equiv$ not =

A = B (when A and B are formulae) 
- This means A and B are the **same formula**
- This does **not** mean A and B have the **same truth table**

A $\equiv$ B:
- A and B have the same truth table ( [[Truth Tables]])
- They may be different formulae
- Is not a logical connective, its comparing A and B
- If something is logically equivalent to $\top$ or $\bot$ then it is a tautology or contradiction respectively


#### Theorem
Let A and B be wff 
$A \equiv B$ precisely when $\vdash A \iff B$
($A \iff B$ is a tautology)


Example: $P, \neg \neg P$
$P \neq \neg \neg P$
but they have the same truth table so
$P \equiv \neg \neg P$
Not a logical connective, its comparing them

We write $A \equiv B$ if A and B have the same truth table - use all the atoms in A and B 

### Equivalences (IMPORTANT)
You **need** to memorise these for the final

**De Morgan's Laws**
1.  $\neg (A \lor B) \equiv \neg A \land \neg B$
2.  $\neg (A \land B) \equiv \neg A \lor \neg B$

**Associativity of $\lor$**
- $(p \lor q) \lor r \equiv p \lor (q \lor r)$

**Commutativity of $\lor$**
- $p \lor q \equiv q \lor p$

**Identity Laws**
- $p \lor \bot \equiv p$
- $p \land \top \equiv p$

**Distributive laws**
- $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$
- $p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$


- p $\lor$ $\neg$p $\equiv$ $\top$
- p $\land$ $\neg$p $\equiv$ $\bot$

**Idempotent laws**
- $p \land p \equiv p$
- $p \lor p \equiv p$

**Absorption Laws**
- $p \lor (p \land q) \equiv p$
- $p \land (p \lor q) \equiv p$

If you only have $\lor$ or only have $\land$, brackets do not affect the answer


### Examples
Unless otherwise specified, using [[Truth Tables]] is generally the easiest way to prove equivalence

**Example**: 
compare p with (p $\land$ (q $\lor$ $\neg$ q))

| $p$ | $q$ | $\neg q$ | $(q \lor \neg q)$ | $(p \land (q \lor \neg q))$ |
| --- | --- | -------- | ----------------- | --------------------------- |
| T   | T   | F        | T                 | T                           |
| T   | F   | T        | T                 | T                           |
| F   | T   | F        | T                 | F                           |
| F   | F   | T        | T                 | F                           |
$p \equiv (p \land(q \lor \neg q))$


**Example:** 
show that $\neg (p \lor q) \equiv \neg p \land \neg q$

| $p$ | $q$ | $\neg p$ | $\neg q$ | $p \lor q$ | $\neg (p \lor q)$ | $\neg p \land \neg q$ |
| --- | --- | -------- | -------- | ---------- | ----------------- | --------------------- |
| T   | T   | F        | F        | T          | F                 | F                     |
| T   | F   | F        | T        | T          | F                 | F                     |
| F   | T   | T        | F        | T          | F                 | F                     |
| F   | F   | T        | T        | F          | T                 | T                     |


**Example:** 
Prove $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$

| p   | q   | r   | $p \land q$ | $q \lor r$ | $p \land r$ | $p \land (q \lor r)$ | $(p \land q) \lor (p \land r)$ |
| --- | --- | --- | ----------- | ---------- | ----------- | -------------------- | ------------------------------ |
| T   | T   | T   | T           | T          | T           | T                    | T                              |
| T   | T   | F   | T           | T          | F           | T                    | T                              |
| T   | F   | T   | F           | T          | T           | T                    | T                              |
| T   | F   | F   | F           | F          | F           | F                    | F                              |
| F   | T   | T   | F           | T          | F           | F                    | F                              |
| F   | T   | F   | F           | F          | F           | F                    | F                              |
| F   | F   | T   | F           | T          | F           | F                    | F                              |
| F   | F   | F   | F           | F          | F           | F                    | F                              |

**Example:** 
Prove $\neg q \implies \neg p \equiv p \implies q$
because $x \implies y \equiv \neg x \lor y$,
$(\neg q) \implies (\neg p) \equiv \neg (\neg q) \lor (\neg p)$

$(\neg q) \implies (\neg p) \equiv (q) \lor (\neg p)$


**Example:** 
Prove $p \implies (q \implies r)    \equiv   (p \land q) \implies r$
$p \implies (q \implies r)    \equiv$

$\neg p \lor (q \implies r)$
$\neg p \lor (\neg q \lor r)$
$\neg p \lor \neg q \lor r$
$\neg (p \land q) \lor r$
$(p \land q) \implies r$


**Example:** 
Prove $\neg (((p \implies q) \implies p) \implies p) \equiv \bot$

| p   | q   | $(p \implies q)$ | $\implies p$ | $\implies p$ | $\neg$ |
| --- | --- | ---------------- | ------------ | ------------ | ------ |
| T   | T   | T                | T            | T            | F      |
| T   | F   | F                | T            | T            | F      |
| F   | T   | T                | F            | T            | F      |
| F   | F   | T                | F            | T            | F      |
Since the equation is false on every value of $p$ and $q$, it is a contradiction, equivalent to $\bot$