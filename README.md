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
FULL ADDER:
module fulladddataflow(a, b, cin, sum, carry);
    input a;
    input b;
    input cin;
    output sum;
    output carry;
 assign sum=a^b^cin;
 assign carry=(a & b) | (b & cin) | (cin & a);
end module

FULL SUBTRACTOR:
module fulsubdataflow(a, b, cin, diff, borrow);
    input a;
    input b;
    input cin;
    output diff;
    output borrow;
	 wire abar;
	 assign abar= ~ a;
	 assign diff=a^b^cin;
	 assign borrow=(abar & b) | (b & cin) |(cin & abar);

endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**
FULL ADDER:
<img width="1920" height="1200" alt="Screenshot 2025-12-05 083128" src="https://github.com/user-attachments/assets/9bdaa22a-4be7-4e3f-afcb-19c688634e40" />

FULL SUBTRACTOR:
<img width="960" height="600" alt="image" src="https://github.com/user-attachments/assets/d6f46877-5dc8-4b9e-9012-80193ab1a9a1" />

**Output Timing Waveform**
FULL ADDER:
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/ffb79a9b-294e-46d6-bbb9-9e4acd91dac2" />

FULL SUBTRACTOR:
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/3f367987-4528-4b44-b0c0-050c5e136ec4" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



