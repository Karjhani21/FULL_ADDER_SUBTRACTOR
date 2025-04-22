# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:KARJHANI PRIYANKA S B

RegisterNumber:212224040150
*/

FULL-ADDER

module exe_4(sum,count,a,b,cin):

output sum;

output count;

input a;

input b;

input cin;

wire s1,c1,c2;

xor(s1,a,b);

and(c1,s1,cin);

xor(sum,s1,cin);

and(c2,s1,cin);

or(count,c2,c1);

endmodule


FULL-SUBTRACTER

module exe_4(df,bo,a,b,bin);

output df;

output bo;

input a;

input b;

input bin;

wire w1,w2,w3;

assign w1=a^b;

assign w2=(~a&b);

assign w3=(~w1&bin);

assign df=w1^bin;

assign bo=w2|w3;

endmodule

RTL Schematic:
![image](https://github.com/user-attachments/assets/90289fc9-5c1c-47ca-b9c5-75e16c4e4dff)

![image](https://github.com/user-attachments/assets/2da612e8-45ba-4c04-9d51-310b8f6ab5ba)




Output Timing Waveform:
![image](https://github.com/user-attachments/assets/d2ad136f-df96-4ef7-a4b4-c836733e1b60)

![image](https://github.com/user-attachments/assets/9b042333-402e-4445-b8d7-6a7c8dfae175)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



