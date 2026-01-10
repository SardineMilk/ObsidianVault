
1
a

| $p$ | $q$ | $p \implies q$ |
| --- | --- | -------------- |
| 1   | 1   | 1              |
| 1   | 0   | 0              |
| 0   | 1   | 1              |
| 0   | 0   | 1              |

b

| $p$ | $q$ | $p \iff q$ |
| --- | --- | ---------- |
| 1   | 1   | 1          |
| 1   | 0   | 0          |
| 0   | 1   | 0          |
| 0   | 0   | 1          |
c

|     |            |        |            |        |
| --- | ---------- | ------ | ---------- | ------ |
|     |            | $\lor$ |            |        |
|     | $\implies$ |        | $\implies$ |        |
| $p$ | $q$        |        | $\neg$     | $\neg$ |
|     |            |        | $q$        | $r$    |

d

| $p$ | $q$ | $r$ | $p \implies q$ | $\neg q$ | $\neg r$ | $\neg q \implies \neg r$ | $(p \implies q) \lor (\neg q \implies \neg r)$ |
| --- | --- | --- | -------------- | -------- | -------- | ------------------------ | ---------------------------------------------- |
| 1   | 1   | 1   | 1              | 0        | 0        | 1                        | 1                                              |
| 1   | 1   | 0   | 1              | 0        | 1        | 1                        | 1                                              |
| 1   | 0   | 1   | 0              | 1        | 0        | 0                        | 0                                              |
| 1   | 0   | 0   | 0              | 1        | 1        | 1                        | 1                                              |
| 0   | 1   | 1   | 1              | 0        | 0        | 1                        | 1                                              |
| 0   | 1   | 0   | 1              | 0        | 1        | 1                        | 1                                              |
| 0   | 0   | 1   | 1              | 1        | 0        | 0                        | 1                                              |
| 0   | 0   | 0   | 1              | 1        | 1        | 1                        | 1                                              |
e

$(\neg p \land \neg q \land r) \lor (\neg p \land \neg q \land \neg r)$   

2

a

|                   |                                   |                                                                  |                                 |                |
| ----------------- | --------------------------------- | ---------------------------------------------------------------- | ------------------------------- | -------------- |
|                   |                                   | $\neg ((p \land q) \implies r) \iff (p \implies (q \implies r))$ |                                 |                |
|                   |                                   | /                                                                | \                               |                |
|                   | $(p \land q) \implies r$          |                                                                  | $\neg ((p \land q) \implies r)$ |                |
|                   | $\neg(p \implies (q \implies r))$ |                                                                  | $p \implies (q \implies r)$     |                |
|                   | \|                                |                                                                  | \|                              |                |
|                   | $p$                               |                                                                  | $p \land q$                     |                |
|                   | $\neg (q \implies r)$             |                                                                  | $\neg r$                        |                |
|                   | \|                                |                                                                  | \|                              |                |
|                   | $q$                               |                                                                  | $p$                             |                |
|                   | $\neg r$                          |                                                                  | $q$                             |                |
|                   | /\                                |                                                                  | /\                              |                |
| $\neg(p \land q)$ |                                   | $r$                                                              | $\neg p$                        | $q \implies r$ |
| \|\               |                                   | x                                                                | x                               |                |
| $\neg p$          | $\neg q$                          |                                                                  | $\neg q$                        | $r$            |
| x                 | x                                 |                                                                  | x                               | x              |
Because the truth tree of the negation of the formula closes, the original formula is a tautology