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
module exp04(a,b,difference,borrow);
input a,b;
output difference,borrow;
wire x;
xor(difference,a,b);
not(x,a);
and(borrow,x,b);
endmodule
```
## FULL SUBTRACTOR
```
module FullSub04(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
wire p;
assign difference=((a^b)^bin);
not (p,a);
assign borrow=((p&b)|(p&bin)|(b&bin));
endmodule
```
## RTL Diagram:

## HALF SUBTRACTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/5cca02ee-4d13-4488-9dad-a8271ba0eb41)



## FULL SUBTARCTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/237deb53-4873-465f-b113-cba492521063)



## Truthtable:

## HALF SUBTRACTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/c0131042-7751-4360-bb40-a28b898fa6e7)



## FULL SUBTARCTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/38fd7ea4-35df-4947-b64a-3ff5c68b6948)


## Output Waveform:

## HALF SUBTRACTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/d256cdbc-791b-4136-a87b-82482d8144b5)



## FULL SUBTARCTOR

![image](https://github.com/lovelydevil36/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/123564624/d9a45370-3abe-4464-85b7-20e9eb2c2651)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
