# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Procedure
/*Create a project with required entities.

Create a module along with respective file name.

Run the respective programs for the given boolean equations.

Run the module and get the respective RTL outputs.

Create university program(VWF) for getting timing diagram.

Give the respective inputs for timing diagram and obtain the results.
*/
## Program:

/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Yamunaasri T S
RegisterNumber:  212222240117


F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module exp2f1(A,B,C,D,f1);
input A,B,C,D;
output f1;
assign f1=(~B&~D)|(A&B&~C)|(~A&B&D);
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy

module exp2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=(~y&z)|(x&y)|(w&y);
endmodule
/*

## Output:
## COMBINATION USING NAND GATE
### RTL
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
![233444435-4818a840-64c2-483b-a579-1e721d4a128e](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/3b69b110-11cb-4a2d-9dce-ff93826b52c5)


F2=xy’z+x’y’z+w’xy+wx’y+wxy
![233444228-a12416d9-cc9c-4d53-8da7-1eb39e636955](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/6879d8a2-ca40-48f3-aa2e-6de73cc13d7e)


### Timing Diagram
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
![233448490-bde5a4e7-3465-45cb-8e95-49a796d61035](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/fbc8ab14-1ce4-4596-8142-b5d5293a74d5)

F2=xy’z+x’y’z+w’xy+wx’y+wxy
![233446842-1ef9acbf-a8d4-459f-a747-f5e7aae8e322](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/0402187c-2bd4-4820-bfad-1c66e4c59726)



## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
