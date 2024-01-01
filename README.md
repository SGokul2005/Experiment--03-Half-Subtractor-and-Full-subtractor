# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
HALF SUBTRACTOR
````
module halfsub(a,b,differ,borrow);
input a,b;
output differ,borrow;
xor(differ,a,b);
assign borrow = ~a & b;
endmodule
````
FULL SUBTRACTOR
````
module fullsub(a,b,c,borrow,differ);
input a,b,c;
output borrow,differ;
xor(differ,a,b,c);
assign borrow = (~a)&c | (~a)&b | (b&c);
endmodule
````


## Output:

## Truthtable
HALF SUBTRACTOR
![WhatsApp Image 2024-01-01 at 21 08 14_e913df54](https://github.com/SGokul2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147121825/122075db-63db-44d6-9824-18fd12dabd3e)

FULL SUBTRACTOR
![WhatsApp Image 2024-01-01 at 21 08 14_94d7ad01](https://github.com/SGokul2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147121825/a25425cf-31a8-4192-a4c7-6507833c62a5)



##  RTL realization
HALF SUBTRACTOR
![image](https://github.com/SGokul2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147121825/84b5e3bd-ed7f-4b6a-859f-2fae3a265391)
FULL SUBTRACTOR
![image](https://github.com/SGokul2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147121825/1155f890-9dbd-4eca-a55a-206e4448ff4f)
## WAVE form
HALF SUBTRACTOR
![Screenshot 2024-01-01 211044](https://github.com/SGokul2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147121825/054b57eb-d0b9-41cf-94d7-f1368ab980f4)
FULL SUBTRACTOR
![Screenshot 2024-01-01 211224](https://github.com/SGokul2005/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147121825/867ef9a6-2343-43ea-ac02-824a41fa599a)


## Timing diagram 

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
