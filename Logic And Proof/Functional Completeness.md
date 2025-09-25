
p, q, r inputs
fill output with random values

| p   | q   | r   |     |
| --- | --- | --- | --- |
| T   | T   | T   | T   |
| T   | T   | F   | T   |
| T   | F   | T   | F   |
| T   | F   | F   | F   |
| F   | T   | T   | F   |
| F   | T   | F   | F   |
| F   | F   | T   | F   |
| F   | F   | F   | T   |
Find a [[Well-Formed Formulae|well-formed formula]] which has this truth table
- Find a wff that outputs true with the correct inputs, and is false in all other cases
	- Find a wff for each line
	- Combine all wff you have

1. $p \land q \land r$
2. $p \land q \land \neg r$
3. $\neg p \land \neg q \land \neg r$
$(p \land q \land r) \lor  (p \land q \land \neg r) \lor (\neg p \land \neg q \land \neg r)$

If it is a contradiction, use something like $p \land \neg p \land q \land r$

**Disjunctive Normal Form (DNF)**
block - single literal / conjunction of literals
A wff is in disjunctive normal form if it is either a block or a disjunction of blocks

(conjunction = and, disjunction = or)

**Claim:** every wff (A) is logically equivalent to one in DNF
**Proof:** Write out the truth table for A, then apply to procedure for proving [[Functional Completeness]]



**Example:**

| p   | q   |     |
| --- | --- | --- |
| T   | T   | T   |
| T   | F   | T   |
| F   | T   | F   |
| F   | F   | F   |
$(p \land q) \lor (p \land \neg q)$


**Example:** write $p \iff q$ in DNF

| p   | q   | $p \iff q$ |
| --- | --- | ---------- |
| T   | T   | T          |
| T   | F   | F          |
| F   | T   | F          |
| F   | F   | T          |
$(p \land q) \lor (\neg p \land \neg q)$
