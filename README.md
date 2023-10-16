# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Components Required:

1.Hardware – PCs, Cyclone II , USB flasher

2.Software – Quartus prime

## Theory:

Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor

## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. half-subtractor9

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/ad12792c-3564-4529-a027-de2997efedb7)

Sum = X'Y+XY' = X ⊕ Y Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. full-subtractor6

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/7710c885-b5d0-4808-be63-544211e42e5d)

Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule.

## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: Abdul hameed.H

RegisterNumber:  212222050001

## HALF SUBTRACTOR
```
module halfsub(a,b,diff,borrow);
input a,b;
output diff,borrow;
assign diff=a^b;
assign borrow=(~a)&b;
endmodule
```
## FULL SUBTRACTOR
```
module fullsub(a,b,bin,diff,borrow);
input a,b,bin;
output diff,borrow;
assign diff=a^b^bin;
assign borrow=((~a)&b)|(~(a^b))&bin;
endmodule
```
## RTL Diagram:

## HALF SUBTRACTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/298db710-8ae0-46c7-bf92-af7696ae19d8)


## FULL SUBTARCTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/801f2d07-fd50-4eb4-84de-aadcd7474271)


## Truthtable:

## HALF SUBTRACTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/6f1255f0-33a6-4d49-8769-fbb0ee08ee50)


## FULL SUBTARCTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/af7103e9-d05c-4410-a1ee-fc6fd62761de)


## Output Waveform:

## HALF SUBTRACTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/5c489faa-07dd-4f66-8df9-c53dca801fb6)


## FULL SUBTARCTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/949cd7ff-3edf-4a25-9ac1-b56cabf7ced2)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
