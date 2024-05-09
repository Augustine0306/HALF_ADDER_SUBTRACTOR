# Implementation-of-Half-Adder-and-Half Subtractor-circuit

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
![image](https://github.com/Augustine0306/HALF_ADDER_SUBTRACTOR/assets/119404460/9d11bf14-8129-44e5-ad9c-1e60719c74d5)

![image](https://github.com/Augustine0306/HALF_ADDER_SUBTRACTOR/assets/119404460/bc4382c2-2bd5-4758-ac5d-b4aeb1b0b5ad)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

*Half_adder*
```
module halfadd_top(a,b,sum,carry);
input a,b;
output sum,carry; 
 assign sum = a^b;
 assign carry = a & b;
endmodule
```
*Half_subtractor*
```
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
  assign Bo = ~a & b;
endmodule
```
```
Developed by: AUGUSTINE J

RegisterNumber: 212222240015

*/
```
**RTL Schematic**

![image](https://github.com/Augustine0306/HALF_ADDER_SUBTRACTOR/assets/119404460/aff26d19-fa2e-4d88-bd5b-43ce196c7a3d)

**Output/TIMING Waveform**

HALF ADDER:

![image](https://github.com/Augustine0306/HALF_ADDER_SUBTRACTOR/assets/119404460/a8249007-3ba3-4454-ba17-2cba04a8b73e)

HALF SUBTRACTOR:

![image](https://github.com/Augustine0306/HALF_ADDER_SUBTRACTOR/assets/119404460/bf5e8ec7-159d-4e65-9d0e-2fcbe501e5fe)

**Result:**

Thus a  a half adder and half subtractor circuit is designed and its truth table in Quartus using Verilog programming is verified.
