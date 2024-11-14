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

FULL ADDER

![1d481ebd-64af-42c5-813f-beeb8bdbcdaa](https://github.com/user-attachments/assets/5c98be18-c0a2-423f-b516-de37d4b1f08d)

FULL SUBTRACTOR


![ca9f7423-72c2-4d2e-87ff-3599a795578d](https://github.com/user-attachments/assets/8417c188-3499-4f23-9c09-a8d801ee17f1)


**Procedure**

1).Type the program in Quartus software.

2).Compile and run the program.

3).Generate the RTL schematic and save the logic diagram.

4).Create nodes for inputs and outputs to generate the timing diagram.

5).For different input combinations generate the timing diagram.

**Program:**

Full Adder

```
module fulladder(sum, cout, a, b, cin);
output sum;
output cout;
input a;
input b;
input cin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign cout=w2|w3;
endmodule
```

Full Subtractor


```
module fullsub(df,bo,a,b,bin);
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
```

Developed by: Santhose Arockiaraj J 

RegisterNumber: 24900171

**RTL Schematic**

Full Adder

![Screenshot 2024-11-14 225122](https://github.com/user-attachments/assets/064aeb22-94a4-4463-8dda-799549a5d773)

Full Subtractor


![Screenshot 2024-11-15 004622](https://github.com/user-attachments/assets/ab830bb7-3f63-4100-876a-26ac4032e71e)


**Output Timing Waveform**

Full Adder

![Screenshot 2024-11-14 230044](https://github.com/user-attachments/assets/55f9897b-84ad-49a6-997b-82f99ab5699c)

Full Subtractor

![Screenshot 2024-11-15 004809](https://github.com/user-attachments/assets/313ef001-8441-4dc6-8943-0e3f52233036)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



