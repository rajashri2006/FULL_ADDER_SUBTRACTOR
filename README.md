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
![ex4 truthtable](https://github.com/user-attachments/assets/7b61cde1-e027-4d4d-8681-f3a560363d72)

**Procedure**

Write the detailed procedure here

**Program:**

module ex4(a,b,c,sum,carry,difference,borrow);

input a,b,c;

output sum,carry,difference,borrow;

assign sum= (a ^ b ^ c);

assign carry= ( a & b | a & c | b & c);

assign difference= (a ^ b ^ c);

assign borrow= ( ~a & b | ~a & c | b & c);

endmodule



/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:RAJASHRI I RegisterNumber:24900207
*/

**RTL Schematic**
![ex4 dia](https://github.com/user-attachments/assets/aa4b4313-fcd4-46fc-992c-17d766f8a341)

**Output Timing Waveform**
![ex4 wave](https://github.com/user-attachments/assets/d6b26a9e-6da1-4945-af8a-afe4a16f5db0)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



