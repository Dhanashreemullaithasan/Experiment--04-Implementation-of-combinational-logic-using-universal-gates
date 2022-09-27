# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
## Program:
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: Dhanashree.M
RegisterNumber:  212221230018
Using NAND gates:
~~~
module exno4(a,b,c,d,f);

input a,b,c,d;

output f;

wire p,q,r;

assign p=(~c & b & a);

assign q=(~d & c & c & a);

assign r=(c & ~b & a);

assign f=(~(~p & ~q & ~r));

endmodule
~~~
Using NOR gates:
```
module combimation(a,b,c,d,f);

input a,b,c,d;

output f;

wire p,q,r;

assign p=(c & ~b & a);

assign q=(d & ~c & a);

assign r=(c & ~b & a);

assign f=((p | q & |r));

endmodule
```
*/
## RTL realization:

## Output:
Using NAND gate:
![ex4](https://user-images.githubusercontent.com/94165415/192530689-ea3a11d6-2630-4b02-8cfd-ff31f380f216.png)

Using NOR gate:
![ex4()](https://user-images.githubusercontent.com/94165415/192531104-55e2f8d6-d406-4a9e-9888-80b6c5fca8cb.png)



## Timing Diagram:
## Using NAND gate:

![WF1](https://user-images.githubusercontent.com/94165415/192530977-7be91e3b-3af4-4a2b-88fd-5024449bc25c.png)

## Using NOR gate:

![WF2](https://user-images.githubusercontent.com/94165415/192531021-dd8f11e6-2f02-444c-9177-89fb32e2de4b.png)

## Truth Table:
## Using NAND gate:
![tt2](https://user-images.githubusercontent.com/94165415/192534307-deb3e212-d01e-4954-a051-df760ad7e2b1.jpeg)

## Using NOR gate:
![tt1](https://user-images.githubusercontent.com/94165415/192534356-9130da10-28ae-4e02-952b-baa2568cc572.jpeg)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
