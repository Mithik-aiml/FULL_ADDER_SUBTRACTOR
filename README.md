# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

Name:G.Mithik jain

ref no:24001881

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

FULL ADDER:

![full adder truth table](https://github.com/user-attachments/assets/8dc52abc-f393-4a69-92ea-54b69c2d16ec)

FULL SUBRACTOR:

![full sub truth table](https://github.com/user-attachments/assets/7b859964-82ea-473c-b6c2-e03b4cd8bc66)


**Procedure**

Type the program in Quartus software.
Compile and run the program.
Generate the RTL schematic and save the logic diagram.
Create nodes for inputs and outputs to generate the timing diagram.
For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

FULL ADDER:

module fulladder(a,b,c,sum,carry); input a,b,c; output sum,carry; wire w1,w2,w3; assign
sum=a^b^c; assign w1=a&b; assign w2=a&b; assign w3=a&b; assign carry=w1|w2|w3;
endmodule

FULL SUBRACTOR:

module fullsub(a,b,bin,diff,borr); input a,b,bin; output diff,borr; wire w1,w2,w3,w4,w5,w6;
xor g1(diff,a,b,bin); and g2(w4,w2,b); and g3(w5,w1,b); and g4(w6,b,bin); or
g5(borr,w4,w5,w6); endmodule
*/

**RTL Schematic**

FULL ADDER:

![image](https://github.com/user-attachments/assets/a36fe86e-22ce-47dd-87f9-4df2dc73cb6e)

FULL SUBRACTOR:

![image](https://github.com/user-attachments/assets/2f4e66b3-3649-4d45-9f01-a7dfbd3eed67)



**Output Timing Waveform**

FULL ADDER:

![image](https://github.com/user-attachments/assets/88d690af-26a1-4a19-88e1-f4c9f4f998ea)

FULL SUBRACTOR:

![image](https://github.com/user-attachments/assets/cc88d96e-af49-44a6-9999-f5d9f03f5b33)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



