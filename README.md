# fibonacci-checker-with-y86-assembly
## Overview
This Y86 assebly program verifies whether all integers in a given sequence are Fibonacci numbers. It is designed to run on a Y86 simulator.
## Features
- The program reads the sequence starting at memory location 0x700.
- The execution stops, when the program encounters first number that is not fibonacci number or 0. This number is returned in the %rax register.
- If all the numbers in the sequence are fibonacci numbers, the program returns value 0 in the %rax register.
## How It Works
A number n is fibonacci number only if (5*n2 + 4) or (5*n2 – 4) is a perfect square. The program uses this consept to check every number in the sequence.
## Limitations
- The program assumes the number sequence always begins with at least the number 1 and ends with number 0.
## Usage
1. Load the program into a Y86 simulator.
2. Run the program.
3. Inspect the result memory location to determine the outcome
## Author
Created by Alisa Kosola as a course project for the Computer Systems 2024 course at the University of Oulu.
