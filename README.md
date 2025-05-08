Question 21 pts
Category: Twos Complement 120 + 8

Assuming that all numbers are represented in 8-bit two's complement binary, what is the decimal value of the result of adding 120 and 8? Your answer must start with an initial sign, + or -. The rest of your answer must only contain decimal digits.


Question 31 pts
Category: Maximum 4-bit Twos Complement

What is the largest decimal number that can be represented by a two's complement 4-bit binary number? Your answer must only contain decimal digits.


Question 71 pts
Category: Sequential RAM

Which of the following statements is not true?

A. SRAM is used in cache and is faster than DRAM.

B. Read operations on RAM and ROM are not controlled by a clock.

C. SRAM and DRAM do not need power to maintain data.

D. The width of a word could vary in different systems.

Group of answer choices

A

B

D

C



Question 81 pts
Category: CPU Wiring
![image](https://github.com/user-attachments/assets/4a500961-6105-473c-b27f-211b7814ef14)

Look at the following (incomplete) diagram of the Hack CPU. Look at the wire (actually, this is a bundle of wires) pointed to by the large red arrow.

Where does the signal on these wires come from and what action does this signal trigger?

CPU-3.png

Group of answer choices

These wires are c1 through to c6 wires of the instruction when we have a C-instruction (when we have an A instruction we either ignore the output of the ALU or "and" the input of these wires with one of the bits indicating that this is a C instruction). Their purpose is to determine where the result of the ALU goes. 

These wires are the rightmost 15 wires of an A-instruction and they are used to put values into the A-register from the ALU. If we have a C-instruction, the circuit is wired such that these wires are ignored.

These wires are c1 through to c6 wires of the instruction when we have a C-instruction (when we have an A instruction we either ignore the output of the ALU or "and" the input of these wires with one of the bits indicating that this is a C instruction). Their purpose is to determine the operations we perform on the ALU.

The wires are the right most bits of the C-instruction (when we have an A instruction we either ignore the output of the ALU or "and" the input of these wires with one of the bits indicating that this is a C instruction) these bits determine if or how we jump. These bits feed into the logic of the ALU and make it produce the relevant bits for updating the PC to determine what instructions to execute next.



Question 101 pts
Category: Assembler

What does the following Hack assembler code do?

        @pix
        M=1
        D=M
        M=M+D
        M=M+1
        D=M
        M=M+D
        M=M+1
        D=M
        @SCREEN
        M=D
 (END)
        @END
        0;JMP
Group of answer choices

It draws one pixel black.

It draws the topmost leftmost three pixels on the screen black.

It draws the following pixels black, pixel 0, pixel 16 and pixel 32.

It draws no pixels black because of overflow.



Question 111 pts
Category: Assembler

What does the following Hack assembler code always do to the current value in RAM location 93?

        @93
        D=!M
        D=D+1
Group of answer choices

It sets RAM[93] to be -RAM[93]

It does not change RAM[93]

It sets RAM[93] to be D + 1

It inverts all the bits in RAM[93]

It sets RAM[93] to be 0


Question 121 pts
Category: Assembly to Hack

Match the following Hack Assembly Language instructions to their 16-bit binary representation.

Group of answer choices
@0

[ Choose ]
0

[ Choose ]
0;JMP

[ Choose ]
A=M

[ Choose ]
A=D+M;JLT

[ Choose ]
@10



Question 131 pts
Category: Assembler Symbols

What three kinds of symbols can appear in a Hack Assembly Language program?

Group of answer choices

labels

constants

virtual registers

variables

predefined

VM control pointers

I/O pointers



Question 161 pts
Category: VM to Assembler push constant 0

Which of the following fragments of Hack assembly language would implement the following virtual machine command? If there is more than one correct answer, select all of them.

push constant 0
Group of answer choices

@0
D=A
@SP
A=M
M=D
@SP
AM=M+1


@SP
M=M+1
A=M
M=0
@SP

A=0
M=M+1
AD=M-1
M=0

@0
D=A
@SP
M=D
@SP
M=M+1

@SP
A=M
M=0
@SP
M=M+1

@0
D=A
@SP
M=M+1
A=M
M=D
@SP



Question 171 pts
Category: VM to Assembler push constant 2

Which of the following fragments of Hack assembly language would implement the following virtual machine command? If there is more than one correct answer, select all of them.

push constant 2
Group of answer choices

@2
D=A
@SP
A=M
M=D
@SP
AM=M+1
 


@SP
A=M
M=1
M=M+1
@SP
M=M+1
 


@2
D=A
@SP
M=M+1
A=M
M=D

A=0
M=M+1
AD=M-1
M=1
M=M+1

@0
D=A
@SP
M=D
@SP
M=M+1

@SP
M=M+1
A=M
M=2
@SP
