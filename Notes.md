# Summary of Notes 

Here are notes for CPU and and Memory. 

# CPU (IR = Instruction Register)

Data is in general purpose register GPR. 


short GPR [4]
bit[12] PC
short IR, MAR, MBR
setR(add, value)
setPC(value);
singleSetRegister
{

	1. Fetch the address the value at PC and move it into IR. 

	2. Parse the value at IR 
		- Return an array of parameters. 

	3. Implement method 
		- Takes an array of parameters
		- Compute effective address (I, Address)
		- Call load(address, R)
			- Call set R
}


# Memory

Memory

Need to declare memory. 
Need to initialize the memory. 
Need to set the memory. 

Code: 

short[2048];
initialize();
set(add; value);

This is the Change...
