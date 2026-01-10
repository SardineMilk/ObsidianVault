1
a *4/4*

| $p$ | $q$ | $p \implies q$ |
| --- | --- | -------------- |
| 1   | 1   | 1              |
| 1   | 0   | 0              |
| 0   | 1   | 1              |
| 0   | 0   | 1              |

b *4/4*

| $p$ | $q$ | $p \iff q$ |
| --- | --- | ---------- |
| 1   | 1   | 1          |
| 1   | 0   | 0          |
| 0   | 1   | 0          |
| 0   | 0   | 1          |
c *4/4*

|     |            |        |            |        |
| --- | ---------- | ------ | ---------- | ------ |
|     |            | $\lor$ |            |        |
|     | $\implies$ |        | $\implies$ |        |
| p   | q          |        | $\neg$     | $\neg$ |
|     |            |        | p          | r      |
d *4/4*

| $p$ | $q$ | $r$ | $p \implies q$ | $\neg p \implies \neg r$ | $(p \implies q) \lor (\neg p \implies \neg r)$ |
| --- | --- | --- | -------------- | ------------------------ | ---------------------------------------------- |
| 1   | 1   | 1   | 1              | 1                        | 1                                              |
| 1   | 1   | 0   | 1              | 1                        | 1                                              |
| 1   | 0   | 1   | 0              | 1                        | 1                                              |
| 1   | 0   | 0   | 0              | 1                        | 1                                              |
| 0   | 1   | 1   | 1              | 0                        | 1                                              |
| 0   | 1   | 0   | 1              | 1                        | 1                                              |
| 0   | 0   | 1   | 1              | 0                        | 1                                              |
| 0   | 0   | 0   | 1              | 1                        | 1                                              |
e *4/4*
FFT
FFF

$(\neg p \land \neg q \land r) \lor (\neg p \land \neg q \land \neg r)$

2.
a *4/4*

| $p$ | $q$ | $r$ | $p \land q$ | $(p \land q) \implies r$ | $q \implies r$ | $p \implies (q \implies r)$ | $((p \land q) \implies r) \iff (p \implies (q \implies r))$ |
| --- | --- | --- | ----------- | ------------------------ | -------------- | --------------------------- | ----------------------------------------------------------- |
| 1   | 1   | 1   | 1           | 1                        | 1              | 1                           | 1                                                           |
| 1   | 1   | 0   | 1           | 0                        | 0              | 0                           | 1                                                           |
| 1   | 0   | 1   | 0           | 1                        | 1              | 1                           | 1                                                           |
| 1   | 0   | 0   | 0           | 1                        | 1              | 1                           | 1                                                           |
| 0   | 1   | 1   | 0           | 1                        | 1              | 1                           | 1                                                           |
| 0   | 1   | 0   | 0           | 1                        | 0              | 1                           | 1                                                           |
| 0   | 0   | 1   | 0           | 1                        | 1              | 1                           | 1                                                           |
| 0   | 0   | 0   | 0           | 1                        | 1              | 1                           | 1                                                           |
All possible outputs of the formula are true, therefore it is a tautology

b *0/4 wrong truth table. should be TFT and FFF* 

| $p$ | $q$ | $r$ | $\neg p \implies q$ | $r \implies q$ | $(\neg p \implies q) \iff (r \implies q)$ | $\neg((\neg p \implies q) \iff (r \implies q))$ |
| --- | --- | --- | ------------------- | -------------- | ----------------------------------------- | ----------------------------------------------- |
| 1   | 1   | 1   | 1                   | 1              | 1                                         | 0                                               |
| 1   | 1   | 0   | 1                   | 1              | 1                                         | 0                                               |
| 1   | 0   | 1   | 1                   | 0              | 0                                         | 1                                               |
| 1   | 0   | 0   | 1                   | 1              | 1                                         | 0                                               |
| 0   | 1   | 1   | 1                   | 1              | 1                                         | 0                                               |
| 0   | 1   | 0   | 0                   | 1              | 0                                         | 1                                               |
| 0   | 0   | 1   | 1                   | 0              | 0                                         | 1                                               |
| 0   | 0   | 0   | 0                   | 1              | 0                                         | 1                                               |
TFT
FTF
FFT
FFF

$(p \land \neg q \land r) \lor (\neg p \land q \land \neg r) \lor (\neg p \land \neg q \land r) \lor (\neg p \land \neg q \land \neg r)$


c *4/4*

$p \implies q, \neg q \vDash \neg p$

| $p$ | $q$ | $p \implies q$ | $\neg q$ | $\neg p$ | $((p \implies q) \land \neg q) \implies \neg p$ |
| --- | --- | -------------- | -------- | -------- | ----------------------------------------------- |
| 1   | 1   | 1              | 0        | 0        | 1                                               |
| 1   | 0   | 0              | 1        | 0        | 1                                               |
| 0   | 1   | 1              | 0        | 1        | 1                                               |
| 0   | 0   | 1              | 1        | 1        | 1                                               |
When the premises $p \implies q$ and $\neg q$ are true, $\neg p$ is true
Therefore the argument is valid

d *4/4 REMEMBER TO DO $\neg \neg p$ AS A STEP*

|     |     |     |                                                                          |     |     |
| --- | --- | --- | ------------------------------------------------------------------------ | --- | --- |
|     |     |     | $\neg (((\neg p \implies q) \land (\neg p \implies \neg q)) \implies p)$ |     |     |
|     |     |     | \|                                                                       |     |     |
|     |     |     | $(\neg p \implies q) \land (\neg p \implies \neg q)$                     |     |     |
|     |     |     | $\neg p$                                                                 |     |     |
|     |     |     | \|                                                                       |     |     |
|     |     |     | $\neg p \implies q$                                                      |     |     |
|     |     |     | $\neg p \implies \neg q$                                                 |     |     |
|     |     |     | /\                                                                       |     |     |
|     | $p$ |     | $\neg q$                                                                 |     |     |
|     | x   |     | /\                                                                       |     |     |
|     |     | $p$ | $q$                                                                      |     |     |
|     |     | x   | x                                                                        |     |     |
The tree of the negation of the formula closes, so the negation of the formula is not satisfiable, so the formula is a tautology

e *4/4*
$p \implies q, q \implies r, r \implies s, p \vDash s$

$((p \implies q) \land (q \implies r) \land (r \implies s) \land p) \implies s$


|     |          |                                                                                       |     |
| --- | -------- | ------------------------------------------------------------------------------------- | --- |
|     |          | $\neg(((p \implies q) \land (q \implies r) \land (r \implies s) \land p) \implies s)$ |     |
|     |          | \|                                                                                    |     |
|     |          | $(p \implies q) \land (q \implies r) \land (r \implies s) \land p$                    |     |
|     |          | $\neg s$                                                                              |     |
|     |          | \|                                                                                    |     |
|     |          | $p$                                                                                   |     |
|     | 1        | $p \implies q$                                                                        |     |
|     | 2        | $q \implies r$                                                                        |     |
|     | 3        | $r \implies s$                                                                        |     |
|     |          | /\                                                                                    |     |
|     | $\neg p$ | $q$                                                                                   |     |
|     | x        | /\|                                                                                   |     |
|     | $\neg q$ | $r$                                                                                   |     |
|     | x        | /\|                                                                                   |     |
|     | $\neg r$ | $s$                                                                                   |     |
|     | x        | x                                                                                     |     |
All branches of the negation close, therefore the formula is a valid argument 

3.
a *4/4*
a * a = a

a = a
a = a * 1 (B6)
a = a * (a + !a) (B9)
a = (a * a) + (a * !a) (B7)
a = (a * a) + 0 (B10)
a = a * a (B3)

b *4/4*
a = a + a

a = a
a = a + 0 (B3)
a = a + (a * !a) (B10)
a = (a + a) * (a + !a) (B8)
a = (a + a) * 1 (B9)
a = a + a (B6)

c *3/3*

A+B+!C
A+B+C
!A+B+C
!A+B+!C
B and nothing else

**put Venn diagram in a frame labelled X**

d *4/4*
ab!c + abc + !abc + !ab!c
ab(!c + c) + !ab(c+!c) (B7)
ab1 + !ab1 (B9)
ab + !ab (B6)
b(a+!a) (B7)
b(1) (B9)
b (B6)





e) *4/4*

| x   | y   | z   | u   | v   |
| --- | --- | --- | --- | --- |
| 1   | 1   | 1   | 1   | 1   |
| 1   | 1   | 0   | 0   | 1   |
| 1   | 0   | 1   | 0   | 1   |
| 1   | 0   | 0   | 0   | 0   |
| 0   | 1   | 1   | 0   | 1   |
| 0   | 1   | 0   | 0   | 0   |
| 0   | 0   | 1   | 0   | 1   |
| 0   | 0   | 0   | 0   | 0   |

u = xyz
v = z + xy 

4
a *0/10*

We define our structure as
D = ({a, b}, {a}, {b})

We interpret P(x) as {a}
We interpret Q(x) as {b}

$(\exists)P(x)$ is true in this structure since ${a} \neq 0$
$(\exists)Q(x)$ is true in this structure since ${b} \neq 0$
It follows that $(\exists)P(x) \land (\exists)Q(x)$ is true in this structure

$P(x) \land Q(x)$ is interpreted as ${a} \cap {b}$, which is empty
It follows that $(\exists x)P(x) \land Q(x)$ is false in this structure


b

|     |       |                          |                                                                                      |     |
| --- | ----- | ------------------------ | ------------------------------------------------------------------------------------ | --- |
|     |       |                          | $\neg ((\exists x)(P(x) \land Q(x)) \implies (\exists x)P(x) \land (\exists x)Q(x))$ |     |
|     |       |                          | \|                                                                                   |     |
|     |       | 1                        | $(\exists x)(P(x) \land Q(x))$                                                       |     |
|     |       | =2                       | $\neg ((\exists x) P(x) \land (\exists x) Q(x))$                                     |     |
|     |       |                          | \|                                                                                   |     |
|     |       | use 1                    | $P(a) \land Q(a)$                                                                    |     |
|     |       |                          | \|                                                                                   |     |
|     |       |                          | $P(a)$                                                                               |     |
|     |       |                          | $Q(a)$                                                                               |     |
|     |       |                          | /\                                                                                   |     |
|     | use 2 | $\neg((\exists x) P(x))$ | $\neg((\exists x) Q(x))$                                                             |     |
|     |       | \|                       | \|                                                                                   |     |
|     |       | $(\forall x) \neg P(x)$  | $(\forall x) \neg Q(x)$                                                              |     |
|     |       | \|                       |                                                                                      |     |
|     |       | $\neg P(a)$              | $\neg Q(a)$                                                                          |     |
|     |       | x                        | x                                                                                    |     |
The truth tree closes, therefore the original formula is universally valid