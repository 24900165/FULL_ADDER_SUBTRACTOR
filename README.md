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


![image](https://github.com/user-attachments/assets/cbf881c8-38ff-4882-acfb-c76e7f7c3fed)


![image](https://github.com/user-attachments/assets/aa6b420f-9296-432c-b826-0e29eb3a7316)



**Procedure**

1.Type the program in the Quartus software.

2.compile and run the program.

3.geenerate the RTL schematic and save the logical diagram.

4.creat the node for the input and output to generate the timing diagram.

5.for the different input combination generate the timing diagram.


**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by:Buvaneshwari.R

RegisterNumber:24900165

module ex_4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor(s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
input module exp_42(df,bo,a,b,bin);
output df;
output bo;
input a
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule


**RTL Schematic**


![image](https://github.com/user-attachments/assets/590cfde6-d1f4-40bd-8a54-1dc5bce0cd09)

![image](https://github.com/user-attachments/assets/55acc94b-ddca-427f-9998-dd7eb76d88a5)



**Output Timing Waveform**


![image](https://github.com/user-attachments/assets/5997c2f6-766e-4524-b5f9-8dffd855931f)


![image](https://github.com/user-attachments/assets/5599891b-3630-4dd7-93ba-ac2936d1cfc7)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



