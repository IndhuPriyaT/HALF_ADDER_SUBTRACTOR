# HALF_ADDER_SUBTRACTOR

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

![image](https://github.com/user-attachments/assets/41869d87-f19c-4c4d-b844-c02ab23d6942)

![image](https://github.com/user-attachments/assets/33e3ef7a-0d53-4113-9055-d7aad7d92069)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

```
/* Program to design a half adder and substractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:Indhu Priya.T
RegisterNumber: 24007533*/
```
```
half_adder
module half_adder(a,b,sum,carry);
input a;
input b;
output sum,carry;
assign sum=a^b;
assign carry=a+b;
endmodule
```
```
half_subtractor
module hs(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference= (a ^ b);
assign borrow= ( ~a & b);
endmodule
```







**RTL Schematic**

# Half Adder
![Screenshot (26)](https://github.com/user-attachments/assets/4c739b12-6353-436c-9cb1-238669aa4c69)


# Half Substractor
![Screenshot (28)](https://github.com/user-attachments/assets/a44ebcb6-ea07-486b-b122-e4a0cab94da6)




**Output/TIMING Waveform**

# Half Adder
![Screenshot (27)](https://github.com/user-attachments/assets/670031b2-2e64-47fe-881b-7eb4894ea3b5)

# Half Substractor
![Screenshot (29)](https://github.com/user-attachments/assets/e4e573cf-9d0a-485b-a426-9a4699b0729c)


**Result:**
Thus designed a half adder and half subtractor circuit and verified its truth table in Quartus using Verilog programming.
