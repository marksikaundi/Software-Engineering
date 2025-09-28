# Computer Architecture Fundamentals: Quiz

## Multiple Choice Questions

1. **What is the primary difference between von Neumann and Harvard architectures?**
   - A) Harvard architecture uses vacuum tubes while von Neumann uses transistors
   - B) Von Neumann architecture uses a single memory for both instructions and data, while Harvard architecture uses separate memories
   - C) Harvard architecture supports only CISC instructions, while von Neumann supports RISC
   - D) Von Neumann architecture is parallel while Harvard is sequential

2. **The von Neumann bottleneck refers to:**
   - A) The limited speed of the ALU in processing complex instructions
   - B) The limitation in performance due to having a single channel for both instruction and data memory access
   - C) The physical size constraints of early computer systems
   - D) The maximum clock speed achievable with vacuum tube technology

3. **Which of the following is NOT a component of the CPU?**
   - A) Control Unit
   - B) Arithmetic Logic Unit
   - C) Registers
   - D) Hard Disk Drive

4. **In a system with a 32-bit address bus, what is the maximum amount of memory that can be directly addressed?**
   - A) 32 Bytes
   - B) 32 MB
   - C) 4 GB
   - D) 32 GB

5. **Which type of bus carries signals that determine whether the CPU is reading from or writing to memory?**
   - A) Address bus
   - B) Data bus
   - C) Control bus
   - D) System bus

6. **Which of the following is NOT a characteristic of RISC architecture?**
   - A) Complex addressing modes
   - B) Fixed instruction length
   - C) Large number of registers
   - D) Load-store architecture

7. **What does the term "cache coherence" refer to?**
   - A) The arrangement of cache memory in hierarchical levels (L1, L2, L3)
   - B) The consistency of data stored in multiple caches in a multiprocessor system
   - C) The physical proximity of cache to the CPU
   - D) The speed at which cache memory operates compared to main memory

8. **Which of the following is an example of spatial locality in memory access?**
   - A) A program repeatedly accessing the same variable in a loop
   - B) A program accessing elements of an array in sequence
   - C) A CPU executing the same subroutine multiple times
   - D) A program using the same set of registers for different operations

9. **In Flynn's taxonomy, what does SIMD represent?**
   - A) Single Instruction, Multiple Data - same operation performed on multiple data points simultaneously
   - B) Single Instruction, Multiple Devices - one instruction controlling multiple hardware devices
   - C) Simultaneous Instruction, Multiple Destinations - parallel execution across multiple cores
   - D) Sequential Instruction, Multiple Decoders - instruction decoding across multiple pipeline stages

10. **Which of the following is a true statement about pipelining?**
    - A) It increases the clock speed of the processor
    - B) It allows multiple instructions to be executed simultaneously in different stages
    - C) It eliminates the need for branch prediction
    - D) It works best with complex, variable-length instructions

## Short Answer Questions

11. **Explain the difference between a combinational circuit and a sequential circuit.**

12. **What is the purpose of the Program Counter (PC) register in the CPU?**

13. **Describe the three main types of hazards in instruction pipelining and how they affect processor performance.**

14. **Explain the concept of virtual memory and why it's important in modern computer systems.**

15. **What is the role of the Translation Lookaside Buffer (TLB) in memory management?**

## Practical Application Questions

16. **Convert the binary number 10110101 to decimal and hexadecimal formats.**

17. **If a computer has a 64-bit data bus and operates at a clock frequency of 3.2 GHz, what is its theoretical maximum data transfer rate in GB/s?**

18. **Design a simple 2-bit counter using D flip-flops and logic gates. Show the circuit diagram and explain its operation.**

19. **Compare and contrast programmed I/O, interrupt-driven I/O, and DMA. For what types of I/O operations would each be most appropriate?**

20. **A processor uses a 4-stage pipeline (Fetch, Decode, Execute, Write-back). If each stage takes 1 clock cycle, calculate the time needed to execute 100 instructions, assuming no pipeline stalls. How does this compare to a non-pipelined execution?**

## Answer Key

1. B
2. B
3. D
4. C
5. C
6. A
7. B
8. B
9. A
10. B

11. A combinational circuit's output depends only on the current input values, with no memory of previous states. A sequential circuit's output depends on both current inputs and previous states, as it contains memory elements like flip-flops.

12. The Program Counter (PC) contains the memory address of the next instruction to be fetched and executed. It's automatically incremented after each instruction fetch unless a jump, branch, or call instruction changes its value.

13. Three main hazards in pipelining:
    - Structural hazards: Multiple instructions competing for the same hardware resource
    - Data hazards: Instructions dependent on results from previous instructions still in the pipeline
    - Control hazards: Branches and jumps disrupting the sequential flow of instructions

14. Virtual memory is a memory management technique that uses disk space as an extension of RAM, providing programs with the illusion of having access to more memory than physically available. It allows multiple programs to run simultaneously, isolates processes from each other, and enables efficient memory utilization through techniques like paging.

15. The TLB is a cache that stores recent translations from virtual to physical addresses. It speeds up virtual memory address translation by avoiding the need to access the page table in main memory for every memory reference.

16. Binary: 10110101
    Decimal: 128 + 32 + 16 + 4 + 1 = 181
    Hexadecimal: B5

17. 64 bits = 8 bytes
    3.2 GHz = 3.2 × 10^9 cycles/second
    Maximum transfer rate = 8 bytes × 3.2 × 10^9 cycles/second = 25.6 GB/s

18. [Circuit diagram would be included here]
    The 2-bit counter uses two D flip-flops to store the current count value. On each clock pulse, the counter increments through the sequence 00, 01, 10, 11, and then repeats. The D input of each flip-flop is connected to appropriate logic to produce the next count value.

19. Programmed I/O: CPU directly controls data transfer and actively polls device status. Simple but inefficient for the CPU.
    Interrupt-driven I/O: Device signals CPU when ready, allowing CPU to perform other tasks while waiting. Better CPU utilization.
    DMA: Hardware controller transfers data without CPU involvement. Most efficient for large data transfers.

    Programmed I/O is suitable for simple devices or infrequent transfers. Interrupt-driven I/O works well for moderate-speed devices like keyboards. DMA is ideal for high-speed devices like disk drives and network interfaces.

20. Non-pipelined: 100 instructions × 4 cycles/instruction = 400 cycles
    Pipelined: 3 cycles (pipeline fill) + 100 instructions = 103 cycles
    The pipelined execution is approximately 3.9 times faster (400/103).
