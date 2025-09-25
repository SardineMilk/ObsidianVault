### Example
Assumptions made are called premises

1. If I swim in the sea, then I will get wet
2. If it rains, then I will get wet
3. Either I swim in the sea or it rains
$\therefore$ I will get wet

$p \implies r$
$q \implies r$
$p \lor q$
$\therefore r$

**Why is this a valid argument?**

| p     | q     | r     | $p \implies r$ | $q \implies r$ | $p \lor q$ |
| ----- | ----- | ----- | -------------- | -------------- | ---------- |
| T     | T     | T     | T              | T              | T          |
| ~~T~~ | ~~T~~ | ~~F~~ | ~~F~~          | ~~F~~          | ~~T~~      |
| T     | F     | T     | T              | T              | T          |
| ~~T~~ | ~~F~~ | ~~F~~ | ~~F~~          | ~~T~~          | ~~T~~      |
| F     | T     | T     | T              | T              | T          |
| ~~F~~ | ~~T~~ | ~~F~~ | ~~T~~          | ~~F~~          | ~~T~~      |
| ~~F~~ | ~~F~~ | ~~T~~ | ~~T~~          | ~~T~~          | ~~F~~      |
| ~~F~~ | ~~F~~ | ~~F~~ | ~~T~~          | ~~T~~          | ~~F~~      |
Cross out any of the rows where not all compound statements are true

The only remaining occurrences of r are true


We write $A_1 , ... , A_n \vdash B$ to mean the when all of A1->An is true then B is also true

We have shown that $p \implies r, q \implies r, p \lor q \vdash r$ 


**Logical Consequence Definition:** 
The argument  $A_1 , ... , A_n \therefore B$ is valid precisely when  $A_1 , ... , A_n \vdash B$ 



**Theorem:** $A_1 , ... , A_n \vdash B$ is valid precisely when $\vdash (A_\ \land ... \land A_n) \implies B$

**Proof:** Assume that $A_1,...,A_n \vdash B$
There are two cases to consider
1.
All $A_1,...,A_n$ are true
This means $A_1 \land ... \land A_n$ is true
We know B is true
So from the truth table for $\implies$ we know that $(A_1 \land ... \land A_n) \implies B$ is true

2.
Some/All of $A_1, ... ,A_n$ is false
This means $A_1 \land ... \land A_n$ is false
Irrespective of whether B is true or false, $(A_1 \land ... \land A_n) \implies B$ true

**Go in the other direction**
Assume $\vdash (A_1 \land ... \land A_n) \implies B$
Assume all $A_1, ... , A_n$ are true
Then $A_1 \land ... \land A_n$ is true
The only possible value for B is true
This proves that $A_1, ... A_n \vdash B$

