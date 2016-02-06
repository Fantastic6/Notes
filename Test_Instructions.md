# Use Instructions 

There is one text field for the address. 

Thre is one row of switches to set the instruction. You can also set the instruction with the text field. 

There are four rows of switches for the general purpose registers. You can also set the value with the text field. 

There are three text fields for the index registers. You can set the value there. 

The display button can be clicked to check the contents of memory location x where x is an index. 

Teh Single Step Switch will run the instruction. 

# Test Instructions 

## LDR

Instruction: 000001 01 00 0 00001 (1281)

Load register 1 with the contents of memory location 1. 

Steps:

1. Set instruction at address 3. 
2. Store at address 1 the value 5, set PC = 3. 
3. Look at the contents of Register 1. It should be 5. 

## STR

Instruction: 000010 10 01 0 10100 (2644)

Store the contents of register 2 into memory location 21. 

Steps: 

1. Set instruction at index 2. 
2. Set R2 = 7.
3. Set I1 = 1, set PC = 2. 
4. Click SSS. Look at memory location 21. It should be 7. 

## LDA

Instruction: 000011 00 01 1 10100 (3188)

Load register 0 with address 27. 

Steps:

1. Set instruction at index 1. 
2. Set I[1] = 7.
3. Set mem[27] = 15, set PC = 1. 
4. Click SSS. Look at the contents of register 0. It should be 15. 

## LDX

Instruction 101001 00 01 1 00000 (42080)

Load index register from memory location 0

1. Set instruction at index 1. 
2. Set mem[0] = 31, set PC = 1. 
3. Click SSS. Look at the contents of I1. It should be 31. 

## STX

Instruction: 101010 00 10 0 00000 (43136)

Store index register to memory location 0

1. Set insturction at index 1. 
2. Set I2[2] = 31, set PC = 1. 
3. Click SSS. Look at the contents of mem[0]. It should be 31. 


## AMR

Instruction: 000100 11 00 0 00000 (4864)

Add the contents of address 0 with the contents of register 3

1. Set instruction at index 1.
2. Set mem[0] = 7. 
3. Set R[3] = 3, set PC = 1.
4. Click SSS. Look at the contents of R[3]. It should be 10. 

## SMR

Instruction: 000101 11 00 0 00000 (5888)

Subtract the contents of memory location 0 from the contents of register 3. 

1. Set insturction at index 1. 
2. Set mem[0] = 5. 
3. Set R[3] = 3, set PC = 1.
4. Click SSS. Look at the contents R[3]. It should be -2. 


## AIR

Instruction: 000110 11 00 0 00010 (6914)

Add the contents of address 0 to the contents of register 3. 

1. Set instruction at address 1. 
2. Set R[3] = 7, set PC = 1. 
3. Click SSS. Look at the contents R[3]. It should be 9. 


## SIR

Instruction: 000111 11 00 0 11111 (7967)

Subtract the contents of intermediate from the register.

1. Set instruction at address 1. 
2. Set R[3] = 47, set PC = 1. 
3. Click SSS. Look at the contents R[3]. It should be (47 - 31 = 16)