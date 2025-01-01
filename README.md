# FULL_ADDER_SUBTRACTOR

DATE:22.10.2024

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
![image](https://github.com/user-attachments/assets/0705dfa2-7539-42c4-b762-e2cdfd783e56)
![image](https://github.com/user-attachments/assets/fd88feb9-e08f-4e9f-bde1-6767b6d44cce)

**Procedure**
```
 1.Type the program in Quartus software.
 2.Compile and run the program.
 3.Generate the RTL schematic and save the logic diagram.
 4.Create nodes for inputs and outputs to generate the timing diagram.
 5.For different input combinations generate the timing diagram.
```

DEVELOPED BY Adithya sivakumar REFERENCE NO:24006778

**Program:**
~~~
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule
~~~
**RTL Schematic**

![image](https://github.com/user-attachments/assets/d6521601-a477-4c8e-88a1-c9509902bb6d)

![image](https://github.com/user-attachments/assets/e568fdca-e5ab-4292-be12-9a99e1f5ffaa)


**Output Timing Wavediagram**

![image](https://github.com/user-attachments/assets/b8d7cb19-ce2b-4766-b5ef-b5388657abb9)

![image](https://github.com/user-attachments/assets/319ec4b8-814c-41a3-ac17-637ce0665a38)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
