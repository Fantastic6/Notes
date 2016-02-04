# Summary of Notes 

We have four classes: CPU.java, Memory.java, Main.java, and Controller.java

# CPU.java 

There are 4 general purpose registers GPRs. (GPR short [])

There are 3 index registers. We need 4 as index since 0 is reserved for a value as well. (IR short[])

We have one instruction set register. (short)

We have one program counter which is a Bitset since it is 12 bits. 
Need special methods to get and set the bitset. 

Need methods to get and set GPR, IR, and ISR. 

The CPU calls a method called process_instruction. It does the following:

1. Fetches the value that PC is pointing to and moves it to the ISR. 
2. We calculate the opcode of the instruction. 
3. Then, we parse the instruction for the five parameters:
	- Opcode (6 bits)
	- Register (2 bits)
	- Index Register (2 bits)
	- Indirect Addressing ? (1 bit)
	- Address (5 bits)
4. Next, we will use the opcode to determine which instruction to run.
	- 1 - ldr
	- 2 - str
	- 3 - lda
	...
5. We need a method to calculate EA since we need it for multiple instructions. 



# Memory.java

Memory is made up of several parts: 

1. Need to declare memory. (Array of 2048 shorts)
2. Need to initialize the memory. 
3. Need to set the memory. (setter)
4. Need to get the memory. (getter)

# Main.java

# Controller.java


