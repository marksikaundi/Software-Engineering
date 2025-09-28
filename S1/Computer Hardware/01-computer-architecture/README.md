# Module 1: Computer Architecture Fundamentals

## Learning Objectives
By the end of this module, you will be able to:
- Explain the basic organization of a computer system
- Describe the Von Neumann and Harvard architectures
- Understand the fetch-decode-execute cycle
- Identify different types of computer systems and their applications
- Explain the concept of instruction sets and addressing modes
- Understand the role of registers and their types

## Reading Assignments

### Primary Reading: Stallings - Fundamentals of Computer Organization and Architecture
- **Chapter 1**: Introduction and Overview (Pages 1-30)
  - Computer evolution and performance
  - Organization vs. architecture
  - Structure and function
- **Chapter 2**: Computer Evolution and Performance (Pages 31-80)
  - Brief history of computers
  - Designing for performance
  - Pentium and PowerPC evolution
- **Chapter 3**: A Top-Level View of Computer Function and Interconnection (Pages 81-130)
  - Computer components
  - Computer function
  - Interconnection structures
- **Chapter 4**: Cache Memory (Pages 131-180)
  - Cache memory principles
  - Elements of cache design
  - Pentium 4 and PowerPC cache organizations

### Supplementary Reading: Mueller - Upgrading and Repairing PCs
- **Chapter 1**: Development of the PC (Pages 1-50)
  - PC history and evolution
  - Types of personal computers
- **Chapter 2**: PC Components, Features, and System Design (Pages 51-100)
  - System components overview
  - System design considerations

## Key Concepts

### 1. Computer System Organization
```
Input → Processing → Output
   ↑        ↓
   ←─── Storage ───→
```

**Components:**
- **Central Processing Unit (CPU)**: Controls operation of computer and performs data processing
- **Main Memory**: Stores data and programs
- **I/O**: Moves data between computer and external environment
- **System Interconnection**: Communication among CPU, memory, and I/O

### 2. Von Neumann Architecture
**Key Principles:**
- Data and instructions stored in same memory
- Memory is linear sequence of locations
- Execution occurs by fetching instructions from memory
- Instructions executed sequentially unless explicitly modified

**Advantages:**
- Simplicity of design
- Flexibility in programming
- Cost-effective implementation

**Disadvantages:**
- Von Neumann bottleneck (shared bus for data and instructions)
- Security vulnerabilities (data and code in same space)

### 3. Harvard Architecture
**Key Features:**
- Separate memory spaces for instructions and data
- Independent buses for instruction and data access
- Parallel access to instructions and data

**Advantages:**
- Eliminates Von Neumann bottleneck
- Better security (code and data separation)
- Higher performance potential

**Applications:**
- Digital Signal Processors (DSPs)
- Microcontrollers
- Some modern CPU cache designs

### 4. Fetch-Decode-Execute Cycle
1. **FETCH**: Retrieve next instruction from memory
   - Program Counter (PC) contains address of next instruction
   - Instruction loaded into Instruction Register (IR)
   - PC incremented to point to next instruction

2. **DECODE**: Interpret instruction
   - Control unit analyzes instruction opcode
   - Determines required operations and operands
   - Generates control signals

3. **EXECUTE**: Perform instruction
   - ALU performs arithmetic/logical operations
   - Data moved between registers and memory
   - Results stored appropriately

### 5. Instruction Sets
**Components of an Instruction:**
- **Opcode**: Specifies operation to be performed
- **Operand**: Specifies data or address for operation

**Instruction Types:**
- **Data Processing**: Arithmetic and logic operations
- **Data Storage**: Memory operations (load/store)
- **Data Movement**: Transfer data between locations
- **Control**: Alter sequence of execution

**Addressing Modes:**
- **Immediate**: Operand is part of instruction
- **Direct**: Operand address specified in instruction
- **Indirect**: Instruction specifies address of address
- **Register**: Operand located in register
- **Register Indirect**: Register contains operand address

### 6. Computer Performance Factors
**Key Metrics:**
- **Clock Speed**: Frequency of system clock (Hz)
- **Instructions Per Clock (IPC)**: Average instructions executed per clock cycle
- **Memory Access Time**: Time to read/write memory
- **Cache Hit Rate**: Percentage of memory accesses served by cache

**Performance Equation:**
```
Execution Time = Instructions × CPI × Clock Cycle Time

Where:
- Instructions = Number of instructions in program
- CPI = Average Cycles Per Instruction
- Clock Cycle Time = 1 / Clock Frequency
```

## Register Types and Functions

### 1. Program Counter (PC)
- Contains address of next instruction to be fetched
- Automatically incremented after each fetch
- Modified by jump, branch, and call instructions

### 2. Instruction Register (IR)
- Holds current instruction being executed
- Loaded during fetch phase of instruction cycle

### 3. Accumulator
- Primary register for arithmetic operations
- Often serves as implicit operand and result storage

### 4. General Purpose Registers
- Available for programmer use
- Reduce memory access requirements
- Improve program performance

### 5. Status/Flag Registers
- Store condition codes and system status
- Include flags like: Zero, Carry, Overflow, Sign, Parity

### 6. Stack Pointer (SP)
- Points to top of system stack
- Used for subroutine calls and interrupt handling

### 7. Index Registers
- Used for array operations and address calculations
- Support indexed addressing modes

## Computer System Types

### 1. Personal Computers (PCs)
**Characteristics:**
- Single user systems
- General purpose computing
- Cost-effective design
- Modular architecture

**Applications:**
- Office productivity
- Gaming and entertainment
- Software development
- Educational use

### 2. Workstations
**Characteristics:**
- High-performance single-user systems
- Specialized for professional applications
- Enhanced graphics capabilities
- Robust construction

**Applications:**
- Computer-aided design (CAD)
- Scientific computing
- Video editing and rendering
- Financial analysis

### 3. Servers
**Characteristics:**
- Multi-user support
- High reliability and availability
- Scalable architecture
- Network-oriented design

**Applications:**
- Web hosting
- Database management
- File sharing
- Email services

### 4. Mainframes
**Characteristics:**
- Large-scale multi-user systems
- Extreme reliability
- High I/O capacity
- Concurrent processing

**Applications:**
- Large organization computing
- Transaction processing
- Data warehousing
- Legacy system support

### 5. Supercomputers
**Characteristics:**
- Highest computational performance
- Parallel processing architecture
- Specialized cooling systems
- Custom interconnection networks

**Applications:**
- Weather forecasting
- Scientific simulation
- Cryptography
- Oil exploration

## Study Activities

### Activity 1: Architecture Comparison
Create a comparison table with the following columns:
- Architecture Type
- Memory Organization
- Bus Structure
- Advantages
- Disadvantages
- Example Systems

Compare Von Neumann, Harvard, and Modified Harvard architectures.

### Activity 2: Instruction Cycle Simulation
Draw a flowchart showing the complete instruction cycle including:
- Fetch phase
- Decode phase
- Execute phase
- Interrupt handling (if applicable)

### Activity 3: Performance Calculation
Given the following specifications, calculate system performance:
- Clock speed: 3.0 GHz
- Average CPI: 2.5
- Program with 1 million instructions
- Calculate execution time and MIPS rating

### Activity 4: Register Function Analysis
For a simple processor design, specify:
- Required register types
- Register sizes (bits)
- Specific functions
- Interconnection requirements

## Self-Assessment Questions

### Multiple Choice
1. In Von Neumann architecture, what creates the bottleneck?
   a) CPU processing speed
   b) Memory access speed
   c) Shared bus for instructions and data
   d) Register file size

2. Which phase of instruction execution determines what operation to perform?
   a) Fetch
   b) Decode
   c) Execute
   d) Store

3. What does the Program Counter register contain?
   a) Current instruction
   b) Address of current instruction
   c) Address of next instruction
   d) Result of last operation

### Short Answer
1. Explain the difference between computer organization and computer architecture.
2. Describe three factors that affect computer system performance.
3. Why might a system designer choose Harvard architecture over Von Neumann?

### Problem Solving
1. A processor executes 500 million instructions with an average of 3 cycles per instruction at 2 GHz. Calculate the execution time.

2. Design a simple addressing scheme for a processor with:
   - 16-bit instructions
   - 8 different opcodes
   - 3 addressing modes
   - How many bits are available for operand specification?

## Key Formulas and Equations

### Performance Metrics
- **MIPS** = Instructions / (Execution Time × 10⁶)
- **CPU Time** = Instructions × CPI / Clock Rate
- **Speedup** = Performance₁ / Performance₂ = Execution Time₂ / Execution Time₁

### Memory Access
- **Average Access Time** = Hit Rate × Cache Access Time + Miss Rate × Memory Access Time
- **Miss Rate** = 1 - Hit Rate

### Amdahl's Law
- **Speedup** = 1 / ((1 - P) + P/S)
  - Where P = fraction that can be parallelized
  - S = speedup of parallel portion

## Laboratory Exercises

### Lab 1: System Exploration
Use system utilities to identify:
- CPU type and specifications
- Memory hierarchy (L1, L2, L3 cache sizes)
- System bus speeds
- Installed memory capacity

**Tools:**
- Windows: System Information, CPU-Z
- Linux: lscpu, /proc/cpuinfo, dmidecode
- macOS: System Information, system_profiler

### Lab 2: Performance Benchmarking
Run benchmarks to measure:
- CPU integer performance
- CPU floating-point performance
- Memory bandwidth
- Cache performance

**Recommended Tools:**
- SPEC CPU benchmarks
- Geekbench
- MemTest86
- CrystalMark

## Glossary

**Architecture**: Attributes of a system visible to programmer (instruction set, data types, addressing modes)

**Organization**: Hardware implementation details (control signals, interfaces, memory technology)

**Instruction Set Architecture (ISA)**: Interface between software and hardware

**Microarchitecture**: Implementation of an ISA in a particular processor

**Pipeline**: Overlapping execution of multiple instructions

**Cache**: Small, fast memory between CPU and main memory

**Bus**: Communication pathway between system components

**Register**: High-speed storage location within CPU

**Clock Cycle**: Basic unit of time in synchronous systems

**Throughput**: Number of tasks completed per unit time

## Additional Resources

### Online Materials
- Computer Architecture Simulators:
  - MARS (MIPS Assembler and Runtime Simulator)
  - QtSpim (MIPS Simulator)
  - Y86 Processor Simulator

### Reference Websites
- IEEE Computer Society (www.computer.org)
- ACM Digital Library (dl.acm.org)
- Intel Developer Documentation
- AMD Technical Documentation

### Video Lectures
- MIT OpenCourseWare: Computer System Architecture
- Stanford CS107: Computer Organization & Systems
- UC Berkeley CS61C: Great Ideas in Computer Architecture

## Next Steps
Upon completion of this module, proceed to:
- **Module 2**: System Components and Motherboards
- Complete the module assessment quiz
- Begin hands-on identification exercises with actual hardware components

---
*Estimated Study Time: 12-15 hours*
*Prerequisites: Basic understanding of digital logic and binary arithmetic*
*Last Updated: [Current Date]*
