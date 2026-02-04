### Von Neumann Architecture
CU (COntrol Unit)
ALU (Arithmetic and Logic Unit)
Linked to make CPU (Central Processing Unit)

Computer
- CPU
- Memory
- I/O

CPU
- Registers
- R1 - Program Counter  (PC) - Current line of execution
Memory
- Addresses

### Fetch-Execute Cycle
Repeatedly
- Fetch 
	- Get address from PC register
	- Load instruction into Instruction Register
- Decode
	- Increment PC
	- Configure ALU
	- Fetch data
- Execute
	- Store any results
	- Change PC if needed (branch etc)


#### Accessing Memory
Address is stored in MAR
- Memory Access Register
If writing
- Memory Data Register
- Control signals to transfer MDR contents to address in MAR
If reading
- Control signals to transfer contents at address in MAR, into the MDR
- Data transferred from MDR into destination register

### Registers
Separate sets for Integer and Floating Pont
- improves performance

Registers are *very* fast
- physically close to the execution

#### Interrupts
*Problems in Instruction Register:*
Addresses not recognised
Invalid Operation
Invalid Result
*I/O operation terminates*
*Battery level etc*