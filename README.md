# fibonacci-checker-with-y86-assembly
## Overview
This Y86 assebly program verifies whether all integers in a given sequence are Fibonacci numbers. It is designed to run on a Y86 simulator.
## Features
- The program reads the number sequence starting at memory location 0x700.
- The program goes through the numbers and checks if they are fibonacci numbers.
- The execution stops, when the program encounters first number that is not fibonacci number or 0. This number is returned in the %rax register.
- If all the numbers in the sequence are fibonacci numbers, the program returns value 0 in the %rax register.
## How It Works
A number n is fibonacci number only if (5*n2 + 4) or (5*n2 – 4) is a perfect square. The program uses this consept to check every number in the sequence in same way as in the C implementation below.
```c
bool isPerfectSquare(int x) {
    int s = sqrt(x);
    return (s*s == x);
}
  
// Returns true if n is a Fibonacci Number, else false
bool isFibonacci(int x) {
    return isPerfectSquare(5*x*x + 4) || isPerfectSquare(5*x*x - 4);
}
```
The multiplication subroutine uses the peasant multiplication algorithm.
```c
int32_t res = 0;
int32_t bit = 1 << 16; 

while (bit > num) {
   bit >>= 2;
   }
   
while (bit != 0) {
   if (num >= res + bit) {
      num -= res + bit;
      res = (res >> 1) + bit;
   } else {
      res >>= 1;
   }
   bit >>= 2;
}
```
## Limitations
- The program assumes the number sequence always begins with at least the number 1 and ends with number 0.
- The maximum value for the number to be checked is 1000 (decimal)
## Author
Created by Alisa Kosola as a course project for the Computer Systems 2024 course at the University of Oulu.
