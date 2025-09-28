# Computer Architecture Fundamentals: Exercises

## Section 1: Binary, Hexadecimal, and Data Representation

### Exercise 1.1: Number System Conversion
1. Convert the decimal number 237 to binary.
2. Convert the binary number 11010111 to decimal.
3. Convert the decimal number 175 to hexadecimal.
4. Convert the hexadecimal number 3AF to decimal.
5. Convert the binary number 10111010 to hexadecimal.
6. Convert the hexadecimal number E5 to binary.

### Exercise 1.2: Binary Arithmetic
1. Add the binary numbers 1011 and 1101.
2. Subtract the binary number 1001 from 1110.
3. Multiply the binary numbers 101 and 11.
4. Represent the decimal number -42 in 8-bit two's complement form.
5. Add the 8-bit two's complement numbers 11111010 and 00001110.

### Exercise 1.3: Character Encoding
1. Represent the string "HELLO" in ASCII, showing the binary representation for each character.
2. If the hexadecimal values 48 65 6C 6C 6F represent a text string in ASCII, what does it say?

## Section 2: Digital Logic

### Exercise 2.1: Logic Gates
1. Create a truth table for each of the following gates: AND, OR, NOT, NAND, NOR, XOR, XNOR.
2. Implement an XOR gate using only NAND gates.
3. Implement an OR gate using only NOR gates.

### Exercise 2.2: Boolean Algebra
1. Simplify the Boolean expression: AB + A(B + C) + B(B + C)
2. Use Boolean algebra to prove that (A + B)(A + C) = A + BC
3. Use a Karnaugh map to simplify the function F(A,B,C,D) = ∑(0,2,5,7,8,10,13,15)

### Exercise 2.3: Combinational Circuits
1. Design a 4-to-1 multiplexer using AND, OR, and NOT gates.
2. Create a circuit that compares two 2-bit numbers and outputs 1 if they are equal.
3. Design a full adder circuit and show its truth table.

## Section 3: Computer Architecture

### Exercise 3.1: Von Neumann vs. Harvard Architecture
1. Draw a block diagram of both the Von Neumann and Harvard architectures.
2. List three advantages and disadvantages of each architecture.
3. Give examples of commercial processors that use each architecture.

### Exercise 3.2: CPU Components
1. Draw a block diagram showing the main components of a CPU and their interconnections.
2. Explain the role of each register in a typical CPU (PC, IR, MAR, MDR, etc.).
3. Trace the path of data and control signals during the execution of a simple instruction.

### Exercise 3.3: Instruction Cycle
1. Draw a flowchart of the fetch-decode-execute cycle.
2. For a simple ADD instruction that adds the contents of two registers, detail what happens in each stage of the instruction cycle.
3. Explain how pipelining can improve the performance of this process.

## Section 4: Memory Systems

### Exercise 4.1: Memory Hierarchy
1. Draw a diagram of the memory hierarchy, indicating typical sizes, access times, and costs.
2. Calculate the average memory access time for a system with:
   - Cache access time: 2 ns
   - Main memory access time: 60 ns
   - Cache hit rate: 95%
3. If you add an L2 cache with access time 10 ns and hit rate 80% (measured on L1 misses), recalculate the average access time.

### Exercise 4.2: Cache Memory
1. For a direct-mapped cache with 16 blocks and a main memory of 256 blocks, show how memory blocks map to cache blocks.
2. Simulate the behavior of a 4-block cache with LRU (Least Recently Used) replacement policy for the following memory access sequence: 5, 9, 14, 5, 9, 12, 15, 5, 12, 8.
3. Compare the performance of direct-mapped, set-associative, and fully associative caches.

### Exercise 4.3: Virtual Memory
1. Explain the process of address translation in a virtual memory system.
2. For a system with 4 KB page size and 32-bit virtual addresses, how many entries would be in the page table?
3. If the physical memory is 1 GB, how many bits are needed for the physical page number?

## Section 5: Instruction Set Architecture

### Exercise 5.1: CISC vs RISC
1. Compare CISC and RISC architectures in terms of:
   - Instruction complexity
   - Addressing modes
   - Register usage
   - Execution model
2. Classify the following processors as primarily CISC or RISC: x86, ARM, MIPS, PowerPC.
3. Debate the advantages of CISC vs RISC for different application domains.

### Exercise 5.2: Addressing Modes
1. Describe five common addressing modes with examples.
2. For each addressing mode, give a practical example of when it would be useful.
3. If you have a 32-bit instruction word, how would you efficiently encode different addressing modes?

### Exercise 5.3: Instruction Formats
1. Design an instruction format for a simple 32-bit processor.
2. Show how you would encode the following instruction types:
   - Register-to-register operations
   - Memory load/store operations
   - Branch operations
   - I/O operations
3. Discuss the tradeoffs in your design.

## Section 6: Advanced Topics

### Exercise 6.1: Pipelining
1. Design a 5-stage pipeline for a simple processor.
2. Identify potential hazards in your pipeline design and suggest solutions.
3. Calculate the theoretical speedup for a 100-instruction program running on your pipelined processor versus a non-pipelined version.

### Exercise 6.2: Parallel Processing
1. Compare SIMD, MIMD, SISD, and MISD architectures.
2. Give examples of applications best suited for each type of parallel architecture.
3. Explain how Amdahl's Law limits the performance improvement from parallelization.

### Exercise 6.3: Modern CPU Features
1. Research and explain three advanced features in modern CPUs (e.g., branch prediction, speculative execution, out-of-order execution).
2. Describe how these features can lead to security vulnerabilities (e.g., Spectre, Meltdown).
3. Suggest ways to mitigate these vulnerabilities while maintaining performance.

## Lab Exercises

### Lab 1: Logic Gate Simulator
Using an online logic gate simulator or software like Logisim:
1. Build basic gates (AND, OR, NOT) using only NAND gates.
2. Design and test a half adder and full adder.
3. Create a 4-bit ripple carry adder.

### Lab 2: Assembly Language Programming
Using a simulator like MIPS or ARM:
1. Write a program to calculate the first 10 Fibonacci numbers.
2. Implement a binary search algorithm.
3. Write a subroutine to convert a decimal number to its hexadecimal representation.

### Lab 3: CPU Performance Analysis
1. Using a CPU benchmark tool, measure the performance of your computer on various tasks.
2. Compare performance with and without certain CPU features enabled (if possible).
3. Analyze the impact of different workloads on CPU utilization and performance.
