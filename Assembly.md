Helps understand performance

ARM


HLL -> Compiles into Assembly -> Assembled into Machine Language Program
-> Linked with libraries -> Executable -> loaded into memory


Keep frequently used data in registers, its faster

Registers:
r0 - r15
each are 32 bits
some have special roles
13 general purpose
- low 0-7
- high 8-12
- Perform most 16 bit operations in low, most 32 bit in high

Current Process Status Register
- Stores current flags
- N - negative
- Z  - zero
- C - carry occured
- V - overflow
- -1 + 1 = 0: NZCV = 0110
- $2^{31} - 1 + 1 = -2^{31}$ NZCV = 1001 


R15 
- program counter
R14
- link register
R13 
- stack pointer



Addresses
- Must be divisible by 4
- 32 bit - 4 bytes



Assembly
- Directives
- Opcodes (mnemonics)
- Operands
- Comments
- Symbols (labels)


Instructions
- normally 1 instruction per line
- some lines may expand into multiple instructions
```
ldr r1 =6    // Load the value 6 into register r1
mov r1, r2

variable: .word 42 // When [variable] is used, it will be replaced with 42

getvar: mov r3 r4
		ldr r4, [variable]
		bx lr
```

CPUlator