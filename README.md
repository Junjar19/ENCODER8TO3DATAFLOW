### ENCODER 8TO3 DATAFLOW Modelling

**AIM:**

To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:** Quartus prime

**THEORY**

**Encoder 8 To 3**

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

**Truth Table**

y7	y6	y5	y4	y3	y2	y1	y0	a	b	c
0	0	0	0	0	0	0	0	0	0	0
0	0	0	0	0	0	0	1	0	0	0
0	0	0	0	0	0	1	0	0	0	1
0	0	0	0	0	1	0	0	0	1	0
0	0	0	0	1	0	0	0	1	0	0
0	0	0	1	0	0	0	0	1	0	0
0	0	1	0	0	0	0	0	0	1	0
0	1	0	0	0	0	0	0	0	1	1
1	0	0	0	0	0	0	0	1	0	0
1	1	0	0	0	0	0	0	1	1	0
1	1	1	0	0	0	0	0	1	1	1
1	1	1	1	0	0	0	0	1	1	1
1	1	1	1	1	0	0	0	1	1	1
1	1	1	1	1	1	0	0	1	1	1
![image](https://github.com/user-attachments/assets/81bb90fd-3f98-4538-8eb5-412bb70f8d27)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![Screenshot 2024-11-17 132019](https://github.com/user-attachments/assets/b1157672-7cc6-4120-a509-576097139da7)

Figure 02  Encoder 8 * 3

**Procedure**

1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.

**PROGRAM**

module encoder8to3(a,b,c,y0,y1,y2,y3,y4,y5,y6,y7);
input y0,y1,y2,y3,y4,y5,y6,y7;
output a,b,c;
assign a= ( y4 | y5 | y6 | y7);
assign b= ( y2 | y3 | y6 | y7);
assign c= ( y1 | y3 | y5 | y7);
endmodule

/* Program for Encoder 8 To 3 in Dataflow Modelling and verify its truth table in quartus using Verilog programming. 

Developed by: Junjar U
RegisterNumber: 24008873


**RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling**

![Screenshot 2024-11-18 100149](https://github.com/user-attachments/assets/88ea1ce2-a648-441f-a605-027d4f087a3c)

**TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling**

**RESULTS**

Thus the given encoder 8 to 3 dataflow functions are implemented and their operations are verified using
Verilog programming.




