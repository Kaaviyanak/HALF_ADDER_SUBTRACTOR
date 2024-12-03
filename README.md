![WhatsApp Image 2024-12-03 at 08 19 55_ced295f6](https://github.com/user-attachments/assets/564cbfd6-4abb-4015-b0ce-a29bd2255722)# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Elaiyavan K
RegisterNumber:24900184
*/
## Half adder
```
 
module ha_dataflow(a, b, s, ca); 
    input a; 
    input b; 
    output s; 
    output ca; 
  assign#2 s=a^b; 
  assign#2 ca=a&b; 
endmodule
```
## Half subtractor
```
 
module hs_dataflow(a, b, dif, bor); 
    input a; 
    input b; 
    output dif; 
    output bor; 
  wire abar; 
  assign#3 abar=~a; 
  assign#3 dif=a^b; 
  assign#3 bor=b&abar; 
endmodule
```

**RTL Schematic**
## Half adder
![Screenshot 2024-12-03 084151](https://github.com/user-attachments/assets/6ea8ed05-208b-46e6-b296-f6fb26b88c50)
## Half subtractors
![Screenshot 2024-12-03 084200](https://github.com/user-attachments/assets/dcdaec98-f949-40ce-a1b9-00106581fb54)

**Output/TIMING Waveform**
## Half adder
![WhatsApp Image 2024-12-03 at 08 19 54_135b7aca](https://github.com/user-attachments/assets/6c9dc699-b0e7-4288-819d-ed3f11e3e3cb)

## Half subtractors
![WhatsApp Image 2024-12-03 at 08 19 55_ced295f6](https://github.com/user-attachments/assets/649db044-1c7a-4157-b777-2dbb21927c79)

**Result:
Thus the half subracter and half adder circuits are design and the truth tables are verified using quartus software
**
