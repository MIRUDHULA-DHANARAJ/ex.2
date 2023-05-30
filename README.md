## Ex. No. : 2 
## Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:
## F1:

![WhatsApp Image 2023-05-30 at 2 42 50 PM](https://github.com/MIRUDHULA-DHANARAJ/ex.2/assets/94828147/1699afb0-dd3d-49ab-a591-6280f95b704c)

## F2:

![WhatsApp Image 2023-05-30 at 2 42 50 PM (1)](https://github.com/MIRUDHULA-DHANARAJ/ex.2/assets/94828147/4f6213ae-56aa-415d-a50c-3258210d5c69)



## Truth Table:

## F1:
![WhatsApp Image 2023-05-30 at 2 42 50 PM (3)](https://github.com/MIRUDHULA-DHANARAJ/ex.2/assets/94828147/1a2d1e35-0b87-445b-a5bc-a210bb13e38d)

##F2:

![WhatsApp Image 2023-05-30 at 2 42 51 PM (5)](https://github.com/MIRUDHULA-DHANARAJ/ex.2/assets/94828147/14a9ba0a-1003-44e5-9272-fbb9fe0af60d)




## Program:
```
Developed By: Mirudhula D
Register No.: 212221230060
```
```
module exp2(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire adash,bdash,cdash,ddash,x,y,z,p,q,r;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(x,bdash,ddash);
and(y,adash,b,d);
and(z,a,b,cdash);
or(f1,x,y,z);
and(p,cdash,d);
and(q,a,c);
and(r,b,c);
or(f2,p,q,r);
endmodule
```

## RTL Schematic:

![image](https://github.com/MIRUDHULA-DHANARAJ/ex.2/assets/94828147/63963c28-3e1f-45eb-9c4c-4c00e3d022ab)

## Timing Diagram:


![image](https://github.com/MIRUDHULA-DHANARAJ/ex.2/assets/94828147/0bd5683b-5d98-4398-a05f-01b8f4024503)


## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



