#logic

You can construct all logical connectives from Not + (And/Or)

| English | Symbol     | Name                  |
| ------- | ---------- | --------------------- |
| not     | $\neg$     | negation              |
| and     | $\land$    | conjunction           |
| or      | $\lor$     | disjunction           |
| xor     | $\oplus$   | exclusive disjunction |
| iff     | $\iff$     | biconditional         |
| implies | $\implies$ | conditional           |
| true    | $\top$     | tautology             |
| false   | $\bot$     | contradiction         |
[[Logic-book.pdf#page=19&selection=69,53,111,14|Logic-book, page 19]]


**Hierarchy of Connectives**
When used in a propositional statement, the following hierarchy can be used to limit brackets:
> ¬, ∧, ∨, →, ↔

Not, And, Or, Implies, Iff (with left being used first)
[[Logic-book.pdf#page=22&selection=229,0,241,1|Logic-book, page 22]]
This is similar to BODMAS in arithmetic 


Inputs: 
- 1 = unary connective
- 2 = binary connective


Logical Connectives
-  NOT = "It is not the case that"
-  AND = no temporal connotations, just glues two statements
-  OR = Always inclusive - A $\lor$ B = A, B, A+B
-  XOR = Exclusive - A $\oplus$ B = A, B
- Iff = If and only if
- Implies = Material Implication. 

**Example: Implies**
Birthday $\implies$ Cake 
If it is my birthday I always eat cake. I may also eat cake when it is not my birthday.
This statement is only false if I do not eat cake on my birthday.

**Example: Iff**
Birthday Party $\iff$ Birthday
I will only ever have a birthday party on my birthday.
This statement will be false if I have a birthday party not on my birthday.
This statement will be false if it is my birthday, and I don't have a birthday party.
 
To define these logical connectives, [[Truth Tables]] can be used


**Example 1.1.3**
headlight warning IF ((key out AND door open) AND (headlights OR parking lights))

p = key out
q = door open
r = headlights on
s = parking lights on

t $\iff$ ((p $\land$ q) $\land$ (r $\lor$ s))

| p   | q   | r   | s   | t   |
| --- | --- | --- | --- | --- |
| T   | T   | T   | T   | T   |
| T   | T   | T   | F   | T   |
| T   | T   | F   | T   | T   |
| T   | T   | F   | F   | F   |
| T   | F   | T   | T   | F   |
| T   | F   | T   | F   | F   |
| T   | F   | F   | T   | F   |
| T   | F   | F   | F   | F   |
| F   | T   | T   | T   | F   |
| F   | T   | T   | F   | F   |
| F   | T   | F   | T   | F   |
| F   | T   | F   | F   | F   |
| F   | F   | T   | T   | F   |
| F   | F   | T   | F   | F   |
| F   | F   | F   | T   | F   |
| F   | F   | F   | F   | F   |


> My car has all kinds of warnings both audible and visual. For example, ‘the audible warning for headlamps sounds if the key is removed from the ignition and the driver’s door is open and either the headlamps are on or the parking lamps are on’. Put p equal to the statement ‘the key is removed from the ignition’, put q equal to ‘the driver’s door is open’, put r equal to ‘the headlamps are on’ and put s equal to ‘the parking lamps are on’. Put t equal to ‘the audible warning for the headlamps sounds’. Then t is true if (p ∧ q) ∧ (r ∨ s) is true. Observe that r ∨ s is the correct version of ‘or’ since we need at least the headlamps to be on or the parking lamps to be on, but that should certainly include the possibility that both sets of ‘lamps’ are on. Although the guidebook uses the word ‘if’, I think it is clear that it really means ‘if and only if’. Thus we want t to be true precisely when (p ∧ q) ∧ (r ∨ s) is true. For example, I don’t want the audible warning for the headlamps to sound if the ‘gas’ is low. Thus if (p ∧ q) ∧ (r ∨ s) is true the audible warning for the headlamps sounds and if (p ∧ q) ∧ (r ∨ s) is false, then it doesn’t.

[[Logic-book.pdf#page=20&selection=142,0,274,26|Logic-book, page 20]]


**Example (on board)**

(p $\lor$ q) $\land$ $\neg$(p $\land$ q) = A

| p   | q   | (p$\lor$q) | $\neg$(p$\land$q) | A   |
| --- | --- | ---------- | ----------------- | --- |
| T   | T   | T          | F                 | F   |
| T   | F   | T          | T                 | T   |
| F   | T   | T          | T                 | T   |
| F   | F   | F          | T                 | F   |



$\neg$p $\implies$ $\neg$ q

| p   | q   | r   |
| --- | --- | --- |
| T   | T   | T   |
| T   | F   | T   |
| F   | T   | F   |
| F   | F   | T   |



| a   | b   | c   | a$\implies$b | c$\implies$b | a$\oplus$c | (a$\implies$b)$\land$(b$\implies$b) | ((a$\implies$b)$\land$(b$\implies$b))$\land$(a$\oplus$c) | A   |
| --- | --- | --- | ------------ | ------------ | ---------- | ----------------------------------- | -------------------------------------------------------- | --- |
| T   | T   | T   | T            | T            | F          | T                                   | F                                                        | T   |
| T   | T   | F   | T            | T            | T          | T                                   | T                                                        | T   |
| T   | F   | T   | F            | F            | F          | F                                   | F                                                        | T   |
| T   | F   | F   | F            | T            | T          | F                                   | F                                                        | T   |
| F   | T   | T   | T            | T            | T          | T                                   | T                                                        | T   |
| F   | T   | F   | T            | T            | F          | T                                   | F                                                        | T   |
| F   | F   | T   | T            | F            | T          | F                                   | F                                                        | T   |
| F   | F   | F   | T            | T            | F          | T                                   | F                                                        | T   |


Example: p $\implies$ $\bot$

| p   | $\bot$ | p $\implies$ $\bot$ |
| --- | ------ | ------------------- |
| T   | F      | F                   |
| F   | F      | T                   |

Example: A= ((x $\implies$ z) $\land$ (y $\implies$ z)) $\implies$ ((x $\lor$ y) $\implies$ z)

| x   | y   | z   | (x $\implies$ z) | (y $\implies$ z) | ((x $\implies$ z) $\land$ (y $\implies$ z)) | (x $\lor$ y) | ((x $\lor$ y) $\implies$ z) | A   |
| --- | --- | --- | ---------------- | ---------------- | ------------------------------------------- | ------------ | --------------------------- | --- |
| T   | T   | T   | T                | T                | T                                           | T            | T                           | T   |
| T   | T   | F   | F                | F                | F                                           | T            | F                           | T   |
| T   | F   | T   | T                | T                | T                                           | T            | T                           | T   |
| T   | F   | F   | F                | T                | F                                           | T            | F                           | T   |
| F   | T   | T   | T                | T                | T                                           | T            | T                           | T   |
| F   | T   | F   | T                | F                | F                                           | F            | T                           | T   |
| F   | F   | T   | T                | T                | T                                           | T            | T                           | T   |
| F   | F   | F   | T                | T                | T                                           | F            | T                           | T   |
It is a Tautology ($\top$)
