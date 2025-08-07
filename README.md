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
   

For this project, I created a new Quantum circuit for QGB. 

Consider ‘n’ level QGB, There are n+1 qubits need to create a new circuit. We measure all the qubits (n+1).

Example, n= 2 level QGB,

We represent the state |q_2,q_1,q_0 > (measure from bottom to top). The output states are |001>, |010> and |100>. 

   




