# off-by-one-8bit-cpu
An 8-bit CPU which purposely introduces off-by-one errors in addition. Built on the Mojo V3 FPGA board.

## Instruction Set

Instructions are 16-bits wide. The CPU supports the following instructions:

NOP
Does nothing

SET [reg:dest] [constant]
Sets the value in reg:dest to a constant value

ADD [reg:dest] [reg:src_A] [reg:src_B]
Sets the value in reg:dest to 1 + the sum of the values in reg:src_A and reg:src_B

JMP [reg:src]
Sets the program counter to the value stored in reg:src

JMP [constant]
Sets the program counter to a constant value

## Registers

The CPU has the following 8-bit registers:
### PC
Used as the program counter, this register stores the current instruction address being processed. Begins at 0. While this register is 8-bits wide, only the 7 least significant bits are used.

### A, B, C
These general purpose registers are 8-bits wide.

## Memory

### ROM
The CPU has a 7-bit address bus connecting the core to ROM.

### RAM
None currently. Send a pull request if you want some RAM.
