hello
1111
11
OK
Question 11 pts
Category: Combinational Logic

The Hack ALU has only 18 instructions listed in figure 2.6 of the textbook but there are 26 = 64 possible input wire configurations. Why aren't all of these instructions available?

Group of answer choices

Actually there are 64 instructions possible - in the machine code - but most are redundant so the assembler doesn't give the programmer a way to express these.

Because most of the other instructions would conflict with the 18 instructions that we have - making it so that they don't work properly. 

To implement all 64 instructions would greatly increase the complexity of the processor and for no benefit since we can do almost everything we want with the 18 instructions we have.

The other instructions are mostly slower than the 18 very fast instructions. We don't implement these other instructions because we don't want to slow down the machine. 
