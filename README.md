## NAME:S.VENGADA KRISHNAN
## REGISTER NUMBER: 212223110061




# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

## Theory:
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits. 
Sum = A’B+AB’ =A ⊕ B Carry = AB
#### Figure -01 HALF ADDER 
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/881166b3-0966-425d-b01c-e7e9d867e0dc)


### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
#### Figure -02 FULL ADDER 
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/b30284b0-586c-467b-934b-07530c4f772f)

### Program:
## HALF ADDER
```
module ha(sum,carry,a,b);
output sum,carry;
input a,b;
assign sum=a^b;
assign carry=a&b;
endmodule
```
## FULL ADDER
```
module FULLADDER(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire x,p,q,r;
xor(x,b,c);
xor(sum,x,a);
and(p,a,b);
and(q,b,c);
and(r,a,c);
or(carry,p,q,r);
endmodule
```
### Output:
### RTL
##  HALF ADDER
![d2](https://github.com/SVENGADAKRISHNAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473084/b4bf7059-b7ca-492a-893e-3f53a709d35c)
## FULL ADDER
![d2](https://github.com/SVENGADAKRISHNAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473084/9a3260cb-1fa0-4ce0-aed0-5759ae2b8047)

### TIMING DIAGRAM
## HALF ADDER
![d222](https://github.com/SVENGADAKRISHNAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473084/0ecf1888-306c-48e0-9bb3-10a0872eec77)

## FULL ADDER
![d2222](https://github.com/SVENGADAKRISHNAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473084/a4272856-655f-4929-9641-8353b46c33c2)

### TRUTH TABLE 
## HALF ADDER
![d22222](https://github.com/SVENGADAKRISHNAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473084/3b5e866b-deea-4e46-80ab-50b42d0cbb57)

## FULL ADDER
![d222222](https://github.com/SVENGADAKRISHNAN/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147473084/1a3adfa7-36f2-4f68-a4c4-821ba091f480)


### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming

