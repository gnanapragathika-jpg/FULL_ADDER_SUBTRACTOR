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
FULL ADDER:

<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/4c08ce18-62b4-4f43-bdf9-d4fbd75598ef" />

FULL SUBTRACTOR:

<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/b3299019-eb2a-4503-9016-740503f50d6c" />

**Procedure:**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

Developed by: A.B.GNANA PRAGATHIKA

RegisterNumber:212225230075

FULL ADDER:

module exp3de1(sum, cout, a, b, cin);
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

FULL SUBTRACTOR:

module exp3de2(df, bo, a, b, bin);

    output df;
    output bo;

    input a;
    input b;
    input bin;

    wire w1, w2, w3;

    assign w1 = a ^ b;
    assign df = w1 ^ bin;

    assign w2 = (~a) & b;
    assign w3 = (~w1) & bin;

    assign bo = w2 | w3;

endmodule

**RTL Schematic**
FULL ADDER:

<img width="868" height="495" alt="Screenshot 2026-06-01 111710" src="https://github.com/user-attachments/assets/ceb75ad6-9afc-4e55-b953-e2a0de9d247f" />

FULL SUBTRACTOR:

<img width="813" height="490" alt="Screenshot 2026-06-01 111722" src="https://github.com/user-attachments/assets/1c4a6481-d119-46fc-be36-241acbf1cc1f" />


**Output Timing Waveform**
FULL ADDER:

<img width="1036" height="527" alt="Screenshot 2026-06-01 111929" src="https://github.com/user-attachments/assets/38351b6a-1569-4aa2-89cc-03081cf5caf5" />

FULL SUBTRACTOR:

<img width="1037" height="512" alt="Screenshot 2026-06-01 111942" src="https://github.com/user-attachments/assets/26a3913f-121d-4d22-9eca-329694879212" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



