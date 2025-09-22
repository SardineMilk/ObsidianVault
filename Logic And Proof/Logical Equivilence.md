

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
A $\equiv$ B precisely when $\vdash$ A$\iff$B
(A iff B is a tautology)


Example: P, $\neg$$\neg$P, compare them
P != $\neg$$\neg$P
but they have the same truth table so
P $\equiv$ $\neg$$\neg$P
Not a logical connective, its comparing them


We write A $\equiv$ B if A and B have the same truth table - use all the atoms in A and B 

**De Morgan's Laws** 
1.  $\neg$(A$\lor$B) $\equiv$ $\neg$A $\land$ $\neg$B
2.   $\neg$(A$\land$B) $\equiv$ $\neg$A $\lor$ $\neg$B

**Important equivalences**
Associativity of $\lor$
- (p  q)  r $\equiv$ p  (q $\lor$ r)

Commutativity of $\lor$
- p $\lor$ q $\equiv$ q $\lor$ p

Something
- p $\lor$ $\bot$ $\equiv$ p
- p $\land$ $\top$ $\equiv$ p

Distributive laws
- p $\land$ (q $\lor$ r) $\equiv$ (p $\land$ q) $\lor$ (p $\land$ r)
- p $\lor$ (q $\land$ r) $\equiv$ (p $\lor$ q) $\land$ (p $\lor$ r)

- p $\lor$ $\neg$p $\equiv$ $\top$
- p $\land$ $\neg$p $\equiv$ $\bot$

Idempotent laws
- p $\land$ p $\equiv$ p
- p $\lor$ p $\equiv$ p

Absorption Laws
- p $\lor$ (p $\land$ q) $\equiv$ p
- p $\land$ (p $\lor$ q) $\equiv$ p

If you only have $\lor$ or only have $\land$, brackets do not affect the answer



**Example**: compare p with (p $\land$ (q $\lor$ $\neg$ q))

| p   | q   | $\neg$q | (q $\lor$ $\neg$ q) | (p $\land$ (q $\lor$ $\neg$ q)) |
| --- | --- | ------- | ------------------- | ------------------------------- |
| T   | T   | F       | T                   | T                               |
| T   | F   | T       | T                   | T                               |
| F   | T   | F       | T                   | F                               |
| F   | F   | T       | T                   | F                               |

p $\equiv$ (p $\land$ (q $\lor$ $\neg$ q))


**Example:** show that $\neg$(p$\lor$q) $\equiv$ $\neg$p $\land$ $\neg$ q


| p   | q   | $\neg$p | $\neg$q | p$\lor$q | $\neg$(p$\lor$q) | $\neg$p $\land$ $\neg$ q |
| --- | --- | ------- | ------- | -------- | ---------------- | ------------------------ |
| T   | T   | F       | F       | T        | F                | F                        |
| T   | F   | F       | T       | T        | F                | F                        |
| F   | T   | T       | F       | T        | F                | F                        |
| F   | F   | T       | T       | F        | T                | T                        |


**Example:** Prove $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$


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

**Example:** Prove $\neg q \implies \neg p \equiv p \implies q$
because $x \implies y \equiv \neg x \lor y$,
$(\neg q) \implies (\neg p) \equiv \neg (\neg q) \lor (\neg p)$

$(\neg q) \implies (\neg p) \equiv (q) \lor (\neg p)$

**Example:** prove $p \implies (q \implies r)    \equiv   (p \land q) \implies r$
$p \implies (q \implies r)    \equiv$

$\neg p \lor (q \implies r)$
$\neg p \lor (\neg q \lor r)$
$\neg p \lor \neg q \lor r$
$\neg (p \land q) \lor r$
$(p \land q) \implies r$


**Example:** $\neg (((p \implies q) \implies p) \implies p)$

| p   | q   | $(p \implies q)$ | $\implies p$ | $\implies p$ | $\neg$ |
| --- | --- | ---------------- | ------------ | ------------ | ------ |
| T   | T   | T                | T            | T            | F      |
| T   | F   | F                | T            | T            | F      |
| F   | T   | T                | F            | T            | F      |
| F   | F   | T                | F            | T            | F      |
It is a contradiction