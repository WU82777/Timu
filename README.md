
Question 11 pts
Category: Maximum 3-bit Unsigned

What is the largest decimal number that can be represented by an unsigned 3-bit binary number? Your answer must only contain decimal digits.

answer : 
7



Question 21 pts
Category: Most Negative 8-bit

What is the decimal value of the most negative number that can be represented by an 8-bit two's complement binary number? Your answer must start with a - sign. The rest of your answer must only contain decimal digits.

answer :
要你学号
-128


Question 31 pts
Category: 4-bit Twos Complement -5 + -5

Assuming that all numbers are represented in 4-bit two's complement binary, what is the decimal value of the result of adding -5 and -5? Your answer must start with an initial sign, + or -. The rest of your answer must only contain decimal digits.

answer: -10

Question 41 pts
Category: Unsigned Minimums

What is the decimal value of the smallest number that can be represented by an 8-bit unsigned binary number? Your answer must start with an initial sign, + or -. The rest of your answer must only contain decimal digits.

answer: +0

Question 51 pts
Category: ALU

The following diagram shows the interface to the Hack ALU and the effect of the six control inputs zx, nx, zy, ny, f and no.
![image](https://github.com/user-attachments/assets/eef67170-e51d-4815-a3c8-03be82cca3a2)
Notes:

The values of x1, x2, y1, y2, fout and out must be expressed as true, false or as simplified boolean expressions.
Boolean expressions may include a single x, a single y and the operators &, | and !.
The values of zr and ng must be expressed as true or false.
Your answers must not include any spaces.
What are the values x1, x2, y1, y2, fout and out when the ALU control inputs have the following values?

if zx == 0 then x1 = 
 , then if nx == 1 then x2 =  
if zy == 0 then y1 = 
 , then if ny == 1 then y2 =  
if f == 0 then fout = 
if no == 1 then out = 
What values would be output on the zr and ng wires if the values of x and y are as follows?

if x == 2 and y == 4 then zr = 
if x == 57 and y == -32768 then ng = 

answer:
x1 = x

x2 = !x

y1 = y

y2 = !y

fout = x2 & y2

out = !fout

zr = false

ng = true






Question 61 pts
Category: Sequential DFF

Imagine that you had a data flip-flop DDF and, during successive clock cycles the signal on its input is:

0,0,1,0,1,0,0,1

What is the output of the DFF on these same clock cycles?

Group of answer choices

?,0,0,1,0,1,0,0

0,1,0,1,0,0,1,0

0,0,1,0,1,0,0,0

?,0,1,0,1,0,0,1


answer: ?,0,0,1,0,1,0,0.

Question 71 pts
Category: Circuit HDL

Select the lines of HDL code shown below that will implement a 1-bit register that is wired as shown in this diagram:
![image](https://github.com/user-attachments/assets/56f7d840-d9bb-4c4f-a354-a33383a5b492)




Chip Bit
{
        IN in, load ;
        OUT out ;

        PARTS:
        // select the lines of HDL code that should go here ...
}
Group of answer choices

Mux(a=tomux,b=in,sel=load,out=todff) ;

Mux(a=in,b=tomux,sel=load,out=todff) ;

DFF(in=todff,out=out) ;

DFF(in=out,out=a,out=out) ;

DFF(in=todff,out=tomux,out=out) ;

Mux(a=out,b=in,sel=load,out=todff) ;


answer:
Mux(a=out,b=in,sel=load,out=todff);

Question 81 pts
Category: CPU Wiring

Look at the following (incomplete) diagram of the Hack CPU. Look at the wire (actually, this is a bundle of wires) pointed to by the large red arrow.

Where does the signal on these wires come from and what action does this signal trigger?
![image](https://github.com/user-attachments/assets/65b48353-7a42-457a-bbb1-a0aed66ac37f)

answer ：A
These wires are c1 through to c6 wires of the instruction when we have a C-instruction (when we have an A instruction we either ignore the output of the ALU or "and" the input of these wires with one of the bits indicating that this is a C instruction). Their purpose is to determine where the result of the ALU goes. 

、


Question 91 pts
Category: CPU Wiring

Look at the following (incomplete) diagram of the Hack CPU. Look at the wire pointed to by the large red arrow.

Where does the signal on this wire come from and what action does this signal trigger?
![image](https://github.com/user-attachments/assets/44933d78-84c1-478a-90d0-412dfada4060)
This wire is the "not" of the left-most bit of the instruction (i15) because the ALU Output is connected to input a of the multiplexor. The signal allows an A-instruction to be routed to the A-register where it can be loaded.

The "a" bit of the C-instruction (the fourth bit from the left). This will trigger whether the value routed to A will come from the memory or the D-register.

This is a "not" of the leftmost destination bit of the C-instruction (d1). This allows the A-register to be loaded with the output of the ALU.

The most significant bit of the result produced by the ALU. If the "not" of this bit is one then the Mux will select to load the output of the memory operation in to the A-register. Otherwise it will transmit the value of the program counter to the A register so the next instruction can be loaded.




Question 101 pts
Category: Assembly Equivalence

The following operations are not legal Hack Assembly Language. Which of these operations could be implemented by executing two consecutive Hack Assembly Language instructions? No other registers or memory locations can be modified.

Group of answer choices

M=-2

AD=D*2

@-5

A=A+M

@-17

D=D*2





Question 111 pts
Category: Assembler

How does a programmer finish a program in Hack Assembler?

Group of answer choices

By specifying a label followed by an instruction that unconditionally jumps to itself.

By setting the address of the A register to zero.

By including an instruction that is all zero bits at the end of the code and then jumping conditionally to that instruction.

By using a halt instruction




Question 121 pts
Category: Assembler

Briefly describe what the following Hack assembler code does

        @KBD
        D=M
        @48
        D=D-A
        @num
        M=D
(END)
        @END
        0;JMP
Group of answer choices

It reads the keboard register at the time of the @kbd command  and exits if the scan code is more than 48.

Nothing, there is a syntax error and the code doesn't assemble.

It reads the keyboard code at the time of the first D=M command and subtracts 48 from it and puts the result in "num"

Nothing, there is no way that this code is able to read the keyboard unless the user is able to press the number '48' which doesn't exist on the keyboard. If it could work it would put the value -48 in "num".


Question 151 pts
Category: Assembler Symbol Tables

Consider the following Hack assembly code:

       @R0
       D=M
       @END
       D;JLE
       @counter
       M=D
       @x
       M=D
(LOOP)
       D=D+A
       @LOOP
       D;JGT
(END)
       @END
       0;JMP
Fill in the appropriate symbol table entries below as they would be after the assembler's first pass.

Your answer should be a positive integer or -
Answer - for predefined symbols or other symbols that should not be present in the symbol table following the first pass.

R0	
D	
M	
END	
JLE	
counter	
x	
LOOP	
A	
JGT	
JMP	



Question 161 pts
Category: VM to Assembler push constant 0

Which of the following fragments of Hack assembly language would implement the following virtual machine command? If there is more than one correct answer, select all of them.

push constant 0
Group of answer choices

A=0
M=M+1
AD=M-1
M=0

@SP
A=M
M=0
@SP
M=M+1

@0
D=A
@SP
A=M
M=D
@SP
AM=M+1

@0
D=A
@SP
M=M+1
A=M
M=D
@SP

@SP
M=M+1
A=M
M=0
@SP

@0
D=A
@SP
M=D
@SP
M=M+1







Question 171 pts
Category: VM to Assembler push constant 2

Which of the following fragments of Hack assembly language would implement the following virtual machine command? If there is more than one correct answer, select all of them.

push constant 2
Group of answer choices

@2
D=A
@SP
M=M+1
A=M
M=D

@SP
M=M+1
A=M
M=2
@SP

@0
D=A
@SP
M=D
@SP
M=M+1

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
 


A=0



Question 221 pts
Category: VM

How many memory segments does the Hack Virtual Machine store in the data memory?

Group of answer choices

2

10

5

9

7

11

8
M=M+1
AD=M-1
M=1
M=M+1





Question 231 pts
Category: VM

Which of the following are segments in the Hack Virtual Machine?

Group of answer choices

variable

constant

field

argument

static
