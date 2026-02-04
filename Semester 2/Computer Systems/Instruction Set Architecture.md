Addressing modes
Instructions
Data types
Registers
Memory Architecture
Interrupt  / Exception handling
External I/O

Operations (+, -, /, MOVE etc)
- How many?
- Which ones
- How complex

Operands (x, y)
- How many?
 - Location (memory/register)
 - Types? (int, float, char etc)

Instruction format in memory
- Size - fixed or variable length
- How many formats?



**Load-Store Architecture**
Operations operate on registers
The cannot operate directly on memory

**Stack Architecture**
FIFO (First In First Out)
Not used physically often
Used in JVM

### ARM
3 operand

dest := op1 op op2

ADD d s1 s2

function | op1 addr | op 2 addr | dest addr

### CISC
Complete tasks in as few instructions as possbile

No cost free
- Complex hardware
- Power hungry
- Not optimised for compilers

### RISC
Simple instructions that can be done in a single clock cycle

Designed for compilers
- CISC cannot optimise by e.g. keeping something loaded in register

ARM is RISC
