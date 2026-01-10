#bl 
Will use [[Boolean Algebra]], and things learned in [[Propositional Logic]] reframed in Boolean ways

Circuits are made of [[Logic Gates]], which in turn are made of [[Transistors]]
#### Proof of Concept

Circuit is a black box
M inputs
N outputs

No memory, so the same input always gets the same output

Inputs and Outputs are all either 0 or 1
2^M possible inputs

Construct a truth table

We shall design multiple machines with only one output

**Example:**
Machine with 2 inputs {x, y} and 2 outputs {u, v}

Build a machine:
C1 takes {x, y} and returns {u}
Build another:
C2 takes {x, y} and returns {v}

Then just combine them in a box with the input divided between the machines
- This division is called "fanout"

*This does not work in the real world*
Because of conservation of energy 

We only deal with M inputs, 1 Output

**Example**
3 inputs {x, y, z} 
1 output {u} random

| x   | y   | z   | u   |
| --- | --- | --- | --- |
| 1   | 1   | 1   | 0   |
| 1   | 1   | 0   | 1   |
| 1   | 0   | 1   | 0   |
| 1   | 0   | 0   | 1   |
| 0   | 1   | 1   | 0   |
| 0   | 1   | 0   | 1   |
| 0   | 0   | 1   | 0   |
| 0   | 0   | 0   | 0   |
Only look at the positive outputs

Minterms
- 1 1 0 - $x . y . \bar {z}$
- 1 0 0  - $x . \bar {y} . \bar {z}$
- 0 1 0 - $\bar {x} . y . \bar {z}$

$u = x . y . \bar {z} + x . \bar {y} . \bar {z} + \bar {x} . y . \bar {z}$
This boolean expression represents exactly the input/output behaviour of our machine

**Construct a circuit from this**
$(xy)\bar{z}$
We will construct a parse tree for this minterm

$(xy)\bar{z}$

|     |     |     |     |
| --- | --- | --- | --- |
|     |     | .   |     |
|     | .   |     | -   |
| x   | y   |     | z   |

etc for the other 2

Then, rotate 90 clockwise
Replace the boolean operators with circuit [[Logic Gates]]

**Theorem**
Every combinatorial circuit can be constructed with Not-Gates, And-Gates, Or-Gates, Fan-Out

Every combinatorial circuit can be constructed with Nand-Gates and Fan-Out