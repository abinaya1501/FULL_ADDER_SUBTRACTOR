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
"C:\Users\admin\Desktop\DE LAB\exp 4\WhatsApp Image 2024-11-14 at 16.48.08_5317bd7c.jpg"
Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![WhatsApp Image 2024-12-10 at 11 47 54_c5a1e847](https://github.com/user-attachments/assets/363825b1-a85d-4836-8e5e-f35ee3aab7b1)
![WhatsApp Image 2024-12-10 at 11 47 54_6e4b0812](https://github.com/user-attachments/assets/20aef98b-360f-4d2f-8d45-2621e4ef2a19)






**Procedure**

Write the detailed procedure here

**Program:**
```
module experiment4(df,bo,a,b,bin);
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
```
module exp04(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**
![Screenshot 2024-12-10 113829](https://github.com/user-attachments/assets/3f6c0a4f-38b9-419e-a89a-c135a6f60052)


![exp4](https://github.com/user-attachments/assets/d819917e-eb62-4e4e-ae18-9d156866f565)




**Output Timing Waveform**
![Screenshot 2024-12-10 114136](https://github.com/user-attachments/assets/27abe6b2-e509-49d8-bf7d-ed4793741aa5)

![exp4 (2)](https://github.com/user-attachments/assets/f3574e3f-72d0-4c1d-b609-1c0d8e42729d)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



