# Quantum Galton Board using qiskit
Aim: To generate Quantum Galton Board (QGB) in a Quantum circuit using Qiskit.

Let   n = Total number of levels in Quantum Galton Box (QGB).

So, we need ‘n+1’ bins to collect balls. 
## Example
Consider a 3 level QGB.
   
   n = 3, The dropped ball from the top are collected in bins.

   Total number of bins = n+1 = 4

   **How to represent bins in Binary?** 
   
   1st bin - $2^0$ = 0001
   
   2nd bin - $2^1$ = 0010
   
   3rd bin – $2^2$ = 0100
   
   4th bin – $2^3$ = 1000
   
 ![image](https://github.com/basid4739/Qwomanium-2025/blob/main/QGB.png?raw=true)
   

**For this project, I created a new Quantum circuit for QGB.** 

Consider ‘n’ level QGB, There are n+1 qubits need to create a new circuit. We measure all the qubits (n+1).

Example, n= 2 level QGB,

We represent the state |**q**<sub>2</sub>,**q**<sub>1</sub>,**q**<sub>0</sub> > (measure from bottom to top). The output states are |001>, |010> and |100>. 

![image](https://github.com/basid4739/Qwomanium-2025/blob/main/2_level.png)
![image](https://github.com/basid4739/Qwomanium-2025/blob/main/2_level_output.png)

**How many Quantum gates require to create a circuit?**

I used X, H, CX, CH, and SWAP gates to create circuits.The quantity of each gate for each level are given below.

| n | x | H | CX | CH | SWAP |
| --|-- | --| -- | -- | ---  |
| 1|1|1|1|0|0 |
|2|1|1|2|1|1|
|3|1|1|3|2|3|
|4|1|1|4|3|4|
|5|1|1|5|4|8|
|6|1|1|6|5|9|
|7|1|1|7|6|15|
|8|1|1|8|7|16|
|9|1|1|9|8|24|
|10|1|1|10|9|25|

From the table , for n level QGB need one X gate, one H gate, n CX gates, (n-1) CH gates.

If n is even, Number of SWAP gates = (n/2)^2  $$\(n\over 2)^2$

If n is odd, Number of SWAP gates = ((n-1)/2)^2+(n-1)

Total number of gates = 1+1+n+ (n-1) + (n/2)^2         ( for n is even)----(1)

Total number of gates = 1+1+n+ (n-1) + ((n-1)/2)^2+(n-1)        ( for n is odd)----(2)

Reducing the number of gates, especially the depth, generally helps reduce error in quantum circuits.


  




