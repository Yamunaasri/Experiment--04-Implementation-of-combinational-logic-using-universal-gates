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

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: Yamunaasri
RegisterNumber:  212222240117
### COMBINATION USING NAND GATE
/*
module combone(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P=(~(~C & B & A));
assign Q=(~(~D & C & A));
assign R=(~(C & ~B & A));
assign F=~(P & Q & R);
endmodule
*/

### COMBINATION USING NOR GATE
/*
module combtwo(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = (C & ~B & A);
assign Q = (D & ~C & A);
assign R = (C & ~B & A);
assign S = (~(P | Q | R));
assign F = (~s);
endmodule 
*/


## Output:
## COMBINATION USING NAND GATE
### RTL
![image](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/f507749d-3f2f-4662-80de-edd229b9772e)

### Timing Diagram
![image](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/cca66867-512c-46d6-80bd-02f9b93c6e6d)
### TRUTH TABLE
![image](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/4aa9ced9-f58a-47e6-9fff-17724bafcb5b)

## COMBINATION USING NOR GATE
### RTL
![image](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/00ee1327-6a2d-414e-91d2-6ac1095771f4)

### Timing Diagram
![image](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/dd1ed1ca-9a37-46f9-96ff-e2c0ed56c0b1)

### Truth table
![image](https://github.com/Yamunaasri/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/115707860/7eb48a90-e039-4601-9303-3606f4e6e858)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
