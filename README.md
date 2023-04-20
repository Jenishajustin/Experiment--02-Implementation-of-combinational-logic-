# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime


## Theory
 Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
### Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.
### Using OR gates

## Logic Diagram
## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.
## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: JENISHA.J
RegisterNumber:  212222230056

for  F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module EXP2a (a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = (~b&~d)|(~a&b&d)|(a&b&~c);
endmodule

for F2=xy’z+x’y’z+w’xy+wx’y+wxy

module EXP2b (w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2 = (x&y)|(w&y)|(~y&z);
endmodule
```
## Output:
## RTL realization
### F1
![2a rtl](https://user-images.githubusercontent.com/119405070/233392432-b03fa736-4ee7-46f1-bfe5-32a2ba7df96e.png)

### F2
![2b rtl](https://user-images.githubusercontent.com/119405070/233395506-24b9c881-dfff-4982-bbff-9224c0daec6c.png)

## Timing Diagram
### F1
![2a timing](https://user-images.githubusercontent.com/119405070/233392531-8fa9d0a9-c64a-48f2-bf07-ad726d525ace.png)

### F2
![2b timing](https://user-images.githubusercontent.com/119405070/233397517-7960935c-652c-47c1-a45e-4aabe5b096e4.png)

## Result:
Thus the given logic functions are implemented using NAND, AND and OR gates and their operations are verified using Verilog programming.
