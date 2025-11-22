# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

<img width="1920" height="1140" alt="Screenshot 2025-11-22 224529" src="https://github.com/user-attachments/assets/32067e1a-570f-4c8b-9dc1-37c072a3e987" />

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

<img width="1920" height="1140" alt="Screenshot 2025-11-22 231227" src="https://github.com/user-attachments/assets/dd500165-4b83-4b4c-8b46-3220df414b10" />

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

// Half Adder in Verilog
module half_adder (
    input  wire a, b,     // Inputs
    output wire sum,      // Sum output
    output wire carry     // Carry output
);

    // Logic equations
    assign sum   = a ^ b;   // XOR for sum
    assign carry = a & b;   // AND for carry

endmodule

// Half Subtractor in Verilog
module half_subtractor (
    input  wire a, b,         // Inputs
    output wire diff, borrow  // Outputs
);

    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = ~a & b;    // Borrow when a < b

endmodule



Developed by:viveka

RegisterNumber: 25016820
*/

**RTL Schematic**

**Output/TIMING Waveform**

half_adder

<img width="1911" height="1151" alt="Screenshot 2025-11-22 225646" src="https://github.com/user-attachments/assets/c675ef4a-7113-4318-aa84-458690fbcd7a" />

half_subtractor

<img width="1920" height="1140" alt="Screenshot 2025-11-22 231749" src="https://github.com/user-attachments/assets/06478699-ad05-4493-bcfc-007872395085" />

**Result:**
Thus the program to design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming was executed successfully.
