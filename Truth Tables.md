
Rows of table = Number of inputs(?) ^ 2

First input - Alternating (TFTF)
Second input - Alternating 2 length (TTFF)
Third input - 4 (TTTTFFFF)
And so on, doubling each input.
This guarantees a correct and rapidly constructed table

| A   | B   | A and B |
| --- | --- | ------- |
| F   | F   | F       |
| F   | T   | F       |
| T   | F   | F       |
| T   | T   | T       |

| A   | B   | A or B |
| --- | --- | ------ |
| F   | F   | F      |
| F   | T   | T      |
| T   | F   | T      |
| T   | T   | T      |

| A   | B   | A xor B |
| --- | --- | ------- |
| F   | F   | F       |
| F   | T   | T       |
| T   | F   | T       |
| T   | T   | F       |

| A   | B   | A -> B |
| --- | --- | ------ |
| F   | F   | T      |
| F   | T   | T      |
| T   | F   | F      |
| T   | T   | T      |

| A   | B   | A <-> B |
| --- | --- | ------- |
| F   | F   | T       |
| F   | T   | F       |
| T   | F   | F       |
| T   | T   | T       |