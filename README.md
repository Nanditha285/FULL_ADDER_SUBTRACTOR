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
'''
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Nanditha Shaji
RegisterNumber: 25012970
*/

**full adder**

module exfull (a,b,c,sum,carry);

input a,b,c;

output sum,carry;

xor g1(sum,a,b,c);

assign carry =(a&b)|(b&c)|(c&a);

endmodule 

**full subtractor**
module fullsub(a,b,c,diff,borrow);

input a,b,c;

output diff,borrow;

xor g1(diff,a,b);

assign borrow =(b&c)|(~a&c)|(~a&b);

endmodule
'''

**RTL Schematic**


<img width="1912" height="954" alt="Screenshot 2025-11-19 202936" src="https://github.com/user-attachments/assets/c44e0912-7bc3-41e5-bfbb-4479d913946a" />


**Output Timing Waveform**
<img width="1910" height="993" alt="Screenshot 2025-11-19 101005" src="https://github.com/user-attachments/assets/338b39bf-aa72-4094-b119-c9406b55a680" />

<img width="1898" height="964" alt="Screenshot 2025-11-19 203800" src="https://github.com/user-attachments/assets/ffaabdd7-6916-4ae0-ac51-ac4211955b9f" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



