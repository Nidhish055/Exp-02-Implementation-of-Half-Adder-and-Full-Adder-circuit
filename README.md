## Name:Nidhish B
## Register Number:23014111
## Experiment:03-Implementation of Half Adder and Full Adder circuit
 
## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime

## Theory:
Adders are digital circuits that carry out addition of numbers.

## Half Adder:
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

#### Figure -01 HALF ADDER 
![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Procedure:
Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

## Program:
~~~
module DE3(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule  
~~~

## RTL realization:
![image](https://github.com/Nidhish055/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145979818/5c69aa34-9b65-4281-848f-61c79a2a4643)

## Truth Table:
![image](https://github.com/Nidhish055/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145979818/c3fca81e-ddc4-487a-ac37-ee5d4898b01a)

## Timing Diagram:
![image](https://github.com/Nidhish055/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145979818/7a6fa4fe-88d3-4f7a-8706-8c7fc442d5db)


## Full Adder:
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

#### Figure -02 FULL ADDER 
 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)
 
 ### Procedure:
Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

## Program:
~~~
module de3_1(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b|b&c|a&c;
endmodule
~~~

## RTL realization:
![image](https://github.com/Nidhish055/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145979818/9b634b68-9d76-403f-b727-8dc084976d01)

## Truth Table:
![image](https://github.com/Nidhish055/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145979818/e32af450-ad8e-4072-8f86-69afce03dbfd)

## Timing Diagram:
![image](https://github.com/Nidhish055/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145979818/fcbe9362-5ae1-464b-adbb-b6cef9c68b10)

## Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming.
