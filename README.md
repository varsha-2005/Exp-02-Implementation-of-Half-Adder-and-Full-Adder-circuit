# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: varsha.g
RegisterNumber:  22002003
*/
For HALF ADDER:

module halfadder(a,b,s,c);
input a,b;
output s,c;
xor (s,a,b);
and (c,a,b);
endmodule

For FULL ADDER:

module fulladder(a,b,ci,s,co);
input a,b,ci;
output s,co;
wire d,e,f;
xor (d,a,b);
xor (s,d,ci);
and (e,ci,d);
and (f,a,b);
or (co,e,f);
endmodule
```

Logic symbol & Truthtable
![image](https://user-images.githubusercontent.com/119288183/229416181-0234d9c5-d17a-4c08-8a20-15ec0264a651.png)



### Output:
### RTL
1.for Half adder
![Screenshot (9) (3)](https://user-images.githubusercontent.com/119288183/229416435-3e66951c-7382-4c37-aebe-d7dc43e1a711.png)


2.for Full adder
![image](https://user-images.githubusercontent.com/119288183/229416516-0a726588-89d0-48da-a81a-06d084cf0b7b.png)


### TIMING DIAGRAM
1.half adder

![Screenshot (8) (5)](https://user-images.githubusercontent.com/119288183/229416739-fcf1e70b-4207-4935-b738-134e3ca3501d.png)


2.full adder
![image](https://user-images.githubusercontent.com/119288183/229416798-639c1c21-0473-4bba-b353-fafc543e06c8.png)





### TRUTH TABLE 
half adder

![229415009-13fc766a-8227-4795-b2f3-87740fd7b207](https://user-images.githubusercontent.com/119288183/229416868-bf7a1ca9-e398-4051-9d8d-08c1ac056c7e.png)


full adder

![229415065-504ca044-402c-4ffd-9776-5f845485f093](https://user-images.githubusercontent.com/119288183/229416914-9db1fcb5-ae61-4e51-97be-f6955fd76a1d.png)


### Result:
Thus half adder and full adder circuit is successfully designed and verified its truth table in Quartus using Verilog programming.
About
