# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 

## Logic Diagram
## Procedure

/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: DINESHKARTHIK N
RegisterNumber:  23013921
*/
## Program:

module Verilog1(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1=(~a&(~b)&(~c)&(~d));
assign A2=(a&c&(~d));
assign A3=((~b)&c&(~d));
assign A4=(~a&b&c&d);
assign A5=(b&(~c)&d);
assign F1=A1|A2|A3|A4|A5;
assign B1=(x&(~y)&z);
assign B2=(~x&(~y)&z);
assign B3=(~w&x&y);
assign B4=(w&(~x)&y);
assign B5=(w&y&z);
assign F2=B1|B2|B3|B4|B5;
endmodule

## RTL realization:

![image](https://github.com/dinesh2068/Experiment--02-Implementation-of-combinational-logic-/assets/151390189/220f8013-878d-40a2-acc4-efbc7ab5cee0)




## Timing Diagram:
![image](https://github.com/dinesh2068/Experiment--02-Implementation-of-combinational-logic-/assets/151390189/0144f84a-66b7-4bf1-a7fc-cd916a898594)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
