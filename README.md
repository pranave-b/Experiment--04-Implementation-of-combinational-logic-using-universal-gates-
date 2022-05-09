# Experiment--04-Implementation-of-combinational-logic-using-universal-gates-
 ## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate


## Equipments Required:
### Hardware – PCs, Cyclone II , USB flasher
### Software – Quartus prime
## Theory
```
A universal gate is a logic gate which can implement any Boolean function without the need to use any other type of logic gate. The NOR gate and NAND gate are universal gates. This means that you can create any logical Boolean expression using only NOR gates or only NAND gates. In practice, this is advantageous since NOR and NAND gates are economical and easier to fabricate than other logic gates. Similarly, an OR gate is typically realised as a NOR gate followed by an inverter.
```
## Procedure
```
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.
```

## Program:
```
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.
Developed by: PRANAVE B
RegisterNumber:  212221240040

## F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

module Combination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule

## F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

module norcombination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
not(F,S);
endmodule
```

## Output:
### F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

## Truthtable
![Screenshot (359)](https://user-images.githubusercontent.com/93427208/167299431-5acc1ec0-5c86-40e1-9d05-0e07dcbd5c58.png)


##  RTL realization
![d2](https://user-images.githubusercontent.com/93427208/167299439-ebe0267b-0c25-4019-b5e3-8dc3bbc2b1b7.png)


## Timing diagram 
![Screenshot (360)](https://user-images.githubusercontent.com/93427208/167299446-cddb33dd-7785-4918-adad-74e956bf9748.png)

### F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

## Truthtable
![Screenshot (361)](https://user-images.githubusercontent.com/93427208/167299662-4850c0ab-4253-46ea-9272-c58c9eb73e26.png)

##  RTL realization
![d2 o](https://user-images.githubusercontent.com/93427208/167299682-f823295c-2dc0-4478-bd9a-a9fbc1f1af53.png)

## Timing diagram 
![Screenshot (362)](https://user-images.githubusercontent.com/93427208/167299703-1bb93796-8e5f-4824-bd89-e1d4576907ab.png)

## Result:
Thus implementation of logic functions using NAND and NOR gates is done and its operation is verified in Quartus using Verilog programming.
