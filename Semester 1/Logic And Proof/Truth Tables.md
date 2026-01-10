
Rows of table = Number of inputs(?) ^ 2

First input - Alternating (TFTF)
Second input - Alternating 2 length (TTFF)
Third input - 4 (TTTTFFFF)
And so on, doubling length each input.
This guarantees a correct and rapidly constructed table


#### Tables For Common [[Logical Connectives]]

| $A$ | $\neg A$ |
| --- | -------- |
| T   | F        |
| F   | T        |

| $A$ | $B$ | $A \land B$ |
| --- | --- | ----------- |
| F   | F   | F           |
| F   | T   | F           |
| T   | F   | F           |
| T   | T   | T           |

| $A$ | $B$ | $A \lor B$ |
| --- | --- | ---------- |
| F   | F   | F          |
| F   | T   | T          |
| T   | F   | T          |
| T   | T   | T          |

| $A$ | $B$ | $A \oplus B$ |
| --- | --- | ------------ |
| F   | F   | F            |
| F   | T   | T            |
| T   | F   | T            |
| T   | T   | F            |

| $A$ | $B$ | $A \implies B$ |
| --- | --- | -------------- |
| F   | F   | T              |
| F   | T   | T              |
| T   | F   | F              |
| T   | T   | T              |

| $A$ | $B$ | $A \iff B$ |
| --- | --- | ---------- |
| F   | F   | T          |
| F   | T   | F          |
| T   | F   | F          |
| T   | T   | T          |
