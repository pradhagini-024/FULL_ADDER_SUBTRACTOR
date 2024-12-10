# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Theory**

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

![download](https://github.com/user-attachments/assets/a548191a-cfa8-41c2-ad4c-977ad84be9c0)


![download](https://github.com/user-attachments/assets/9b11ded6-d735-4321-a14d-0e644219254a)


**Procedure**

1. Type the program in Quartus software.
  
2. Compile and run the program.
  
3. Generate the RTL schematic and save the logic diagram.
   
4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram
   
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

i)FULL ADDER

```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```
ii)FULL SUBTRACTOR

```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```

Developed by: Pradhagini A RegisterNumber: 24901125*/

**RTL Schematic**

![exp4 full adder](https://github.com/user-attachments/assets/6e3a3f86-61e7-407c-b852-f8d50e2352c0)

![exp4 fs](https://github.com/user-attachments/assets/d8100773-31e3-4e3e-be14-6a9822842d37)

**Output Timing Waveform**

![exp4 fa wf](https://github.com/user-attachments/assets/e6c5eaec-bc7b-4c6e-9fc8-50e11fa419c8)

![exp4 fs wf](https://github.com/user-attachments/assets/abff7b3b-6c33-42c5-ae54-c5dda9f2bed6)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



