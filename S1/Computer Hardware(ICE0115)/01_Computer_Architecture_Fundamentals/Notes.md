# Computer Architecture Fundamentals: Detailed Notes

## 1.1 Computer System Architecture

### Historical Development
- **First Generation (1945-1955)**: Vacuum tubes, punch cards, machine language programming
- **Second Generation (1955-1965)**: Transistors, assembly language, batch processing
- **Third Generation (1965-1980)**: Integrated circuits, high-level programming languages, multiprogramming
- **Fourth Generation (1980-present)**: VLSI circuits, personal computers, GUIs, internet
- **Fifth Generation (current)**: AI integration, parallel processing, quantum computing

### Von Neumann Architecture
- Developed by mathematician John von Neumann in 1945
- **Key components**:
  - Central Processing Unit (CPU)
  - Memory Unit (stores both data and instructions)
  - Input/Output System
  - Control Unit (coordinates operations)
  - Arithmetic and Logic Unit (performs calculations)
- **Key characteristics**:
  - Stored program concept (instructions stored in memory)
  - Sequential execution of instructions
  - Single data/instruction path (von Neumann bottleneck)

### Harvard Architecture
- Physically separate storage and signal pathways for instructions and data
- Allows simultaneous access to both instructions and data
- Found in many modern microcontrollers and DSPs
- Advantages: Faster execution, parallel access
- Disadvantages: More complex design, higher cost

### Modern System Architectures
- **Modified Harvard Architecture**: Combines elements of both architectures
- **SMP (Symmetric Multiprocessing)**: Multiple identical processors share memory
- **NUMA (Non-Uniform Memory Access)**: Memory access times depend on memory location relative to processor
- **MPP (Massively Parallel Processing)**: Many separate processors with individual memory
- **SOC (System on Chip)**: Entire computer system on a single integrated circuit

### System Buses and Interconnection
- **Address Bus**: Carries memory addresses between CPU and memory
  - Unidirectional (CPU to memory)
  - Width determines maximum memory capacity (e.g., 32-bit = 4GB addressable memory)
- **Data Bus**: Transfers actual data between system components
  - Bidirectional
  - Width affects data transfer rate (8, 16, 32, 64, 128-bit)
- **Control Bus**: Carries control signals
  - Read/write signals, interrupt requests, clock signals
  - Coordinates system operations

## 1.2 Binary Logic and Digital Components

### Number Systems
- **Binary (Base-2)**: Only uses 0 and 1
  - Each position represents a power of 2 (1, 2, 4, 8, 16, etc.)
  - Example: 1011₂ = 1×2³ + 0×2² + 1×2¹ + 1×2⁰ = 8 + 0 + 2 + 1 = 11₁₀
- **Hexadecimal (Base-16)**: Uses digits 0-9 and letters A-F
  - Each hex digit represents 4 binary digits
  - Example: 2A₁₆ = 2×16¹ + 10×16⁰ = 32 + 10 = 42₁₀
  - Binary conversion: 2A₁₆ = 0010 1010₂
- **Data representation**:
  - ASCII: 7-bit coding system for text (128 characters)
  - Unicode: Extended character set supporting multiple languages
  - Binary-coded decimal (BCD): Each decimal digit encoded separately in binary

### Boolean Algebra and Logic Gates
- **Basic operations**:
  - AND (·): Output is 1 only if all inputs are 1
  - OR (+): Output is 1 if at least one input is 1
  - NOT (¯ or '): Inverts the input
- **Derived operations**:
  - NAND: NOT-AND combination
  - NOR: NOT-OR combination
  - XOR (⊕): Output is 1 if inputs are different
  - XNOR: Output is 1 if inputs are the same
- **Basic logic gates**:
  - Implementation of Boolean operations in hardware
  - Fundamental building blocks of digital circuits

### Combinational and Sequential Circuits
- **Combinational circuits**: Output depends only on current input
  - Examples: Multiplexers, decoders, adders
  - No memory or feedback
- **Sequential circuits**: Output depends on current input and previous state
  - Contains memory elements (flip-flops)
  - Examples: Registers, counters, memory units

### Basic Digital Components
- **Flip-flops**: Basic storage element that can be in one of two states
  - Types: SR, JK, D, T flip-flops
  - Edge-triggered vs. level-triggered
- **Registers**: Group of flip-flops used to store multiple bits
  - Data registers, address registers, status registers
- **Counters**: Sequential circuits that count clock pulses
  - Asynchronous (ripple) vs. synchronous counters
- **Arithmetic Logic Unit (ALU)**:
  - Performs arithmetic operations (add, subtract)
  - Performs logical operations (AND, OR, XOR)
  - Core component of the CPU

## 1.3 CPU Organization

### Control Unit and ALU
- **Control Unit (CU)**: Coordinates and directs operations
  - Fetches and decodes instructions
  - Generates control signals
  - Hardwired control vs. microprogrammed control
- **Arithmetic Logic Unit (ALU)**:
  - Performs all arithmetic calculations
  - Handles logical operations
  - Typically connected directly to CPU registers

### Registers and Their Types
- **General Purpose Registers (GPRs)**: Temporary data storage
- **Special Purpose Registers**:
  - **Program Counter (PC)**: Contains address of next instruction
  - **Instruction Register (IR)**: Holds current instruction being executed
  - **Memory Address Register (MAR)**: Holds memory address being accessed
  - **Memory Data Register (MDR)**: Holds data being read/written to memory
  - **Status Register/Flags**: Contains condition codes (zero, carry, overflow, etc.)

### Instruction Formats
- **Instruction components**:
  - Operation code (opcode)
  - Source operand(s)
  - Destination operand(s)
  - Addressing mode specifier
- **Instruction formats**:
  - Fixed-length vs. variable-length
  - 0-address, 1-address, 2-address, 3-address formats
  - RISC typically uses fixed-length, CISC often variable-length

### Addressing Modes
- **Immediate**: Operand is included in instruction
- **Direct**: Instruction contains the address of operand
- **Indirect**: Instruction contains address where the effective address is stored
- **Register**: Operand is in a register
- **Register indirect**: Register contains address of operand
- **Indexed**: Address is sum of a base address and an index register
- **Base-displacement**: Address is sum of a base register and a displacement value

### Instruction Pipelining
- Overlapping execution of multiple instructions
- Typical stages:
  - Instruction Fetch (IF)
  - Instruction Decode (ID)
  - Execute (EX)
  - Memory Access (MEM)
  - Write Back (WB)
- **Hazards**:
  - Structural: Hardware resource conflicts
  - Data: Data dependencies between instructions
  - Control: Branch and jump instructions

### CISC vs RISC Architectures

#### CISC (Complex Instruction Set Computing)
- Many specialized instructions, some rarely used
- Variable instruction length
- Complex addressing modes
- Instructions may take multiple clock cycles
- Examples: x86, x86-64 (Intel, AMD)

#### RISC (Reduced Instruction Set Computing)
- Fewer, simpler instructions
- Fixed instruction length
- Limited addressing modes
- Most instructions execute in one clock cycle
- More registers
- Load-store architecture (only load/store instructions access memory)
- Examples: ARM, MIPS, RISC-V

## 1.4 Memory Organization

### Memory Hierarchy
- **Registers**: Fastest, smallest, most expensive storage in CPU
- **Cache**: Small, fast memory close to CPU
  - L1 Cache: Smallest, fastest, directly on CPU core
  - L2 Cache: Larger, slower, may be shared between cores
  - L3 Cache: Even larger, shared between all cores
- **Main Memory (RAM)**: Primary system memory
  - Volatile (loses data without power)
  - Directly addressable by CPU
- **Secondary Storage**: Non-volatile storage
  - Hard drives, SSDs, optical media
  - Much larger capacity, much slower access

### Cache Memory Principles
- **Temporal locality**: Recently accessed data likely to be accessed again
- **Spatial locality**: Data near recently accessed locations likely to be accessed
- **Cache organization**:
  - Cache line/block: Unit of data transfer between cache and memory
  - Direct-mapped: Each memory location maps to exactly one cache location
  - Fully associative: Memory block can be placed in any cache line
  - Set associative: Compromise between direct-mapped and fully associative
- **Cache coherence**: Maintaining consistent data in multiprocessor systems
  - Write-through vs. write-back policies
  - MESI protocol (Modified, Exclusive, Shared, Invalid)

### Virtual Memory
- Allows programs to use more memory than physically available
- **Paging**: Fixed-size blocks (pages) of memory moved between RAM and disk
  - Page table: Maps virtual addresses to physical addresses
  - Page fault: Occurs when accessed page isn't in physical memory
- **Segmentation**: Variable-sized logical address spaces
- **Translation Lookaside Buffer (TLB)**: Cache for page table entries

### Memory Management Techniques
- **Memory protection**: Prevents processes from accessing each other's memory
- **Memory allocation**: Static vs. dynamic allocation
- **Garbage collection**: Automatic reclamation of unused memory
- **Memory compaction**: Consolidating free memory blocks

## 1.5 I/O Organization

### I/O Modules and Interfaces
- **I/O module functions**:
  - Interface to CPU and memory (via system bus)
  - Interface to external devices
  - Control and timing
  - Error detection
- **I/O interfaces**:
  - Parallel interfaces: Multiple bits transferred simultaneously
  - Serial interfaces: Bits transferred one at a time
  - Standardized interfaces: USB, SATA, PCIe, etc.

### I/O Techniques

#### Programmed I/O
- CPU directly controls I/O operations
- CPU enters wait loop until device ready
- Simple but inefficient (wastes CPU cycles)

#### Interrupt-driven I/O
- Device signals CPU when ready (via interrupt)
- CPU can perform other tasks while waiting
- **Interrupt handling process**:
  1. Device raises interrupt signal
  2. CPU completes current instruction
  3. CPU saves current state
  4. CPU executes interrupt service routine (ISR)
  5. CPU restores state and continues

#### Direct Memory Access (DMA)
- Allows devices to transfer data directly to/from memory without CPU involvement
- CPU initiates transfer, then DMA controller takes over
- CPU notified when transfer complete
- Greatly reduces CPU overhead for large transfers

### I/O Channels and Processors
- Specialized processors that handle I/O operations
- Execute channel programs (I/O instructions)
- Allow CPU to offload I/O management
- Types: Selector channels, multiplexer channels

## 1.6 Modern Architectural Enhancements

### Parallel Processing Concepts
- **Flynn's Taxonomy**:
  - SISD (Single Instruction, Single Data): Traditional von Neumann
  - SIMD (Single Instruction, Multiple Data): Vector/array processing
  - MISD (Multiple Instruction, Single Data): Rarely implemented
  - MIMD (Multiple Instruction, Multiple Data): Multicore, multiprocessor
- **Levels of parallelism**:
  - Bit-level: Process more bits simultaneously
  - Instruction-level: Execute multiple instructions simultaneously
  - Data-level: Same operation on multiple data elements
  - Task-level: Multiple threads/processes execute simultaneously

### Multicore Processors
- Multiple CPU cores on a single chip
- Shared cache (typically L3) and memory controller
- Advantages: Improved performance, reduced power consumption
- Challenges: Heat dissipation, programming complexity
- **Core types**:
  - Homogeneous: All cores identical
  - Heterogeneous: Different cores for different workloads (e.g., big.LITTLE)

### Superscalar and Out-of-order Execution
- **Superscalar**: Multiple instructions issued per clock cycle
  - Multiple execution units (ALUs, FPUs, etc.)
  - Instruction-level parallelism
- **Out-of-order execution**: Instructions executed in order that maximizes throughput
  - Instruction reordering to avoid stalls
  - Register renaming to eliminate false dependencies
  - Speculative execution
- **Branch prediction**: Attempts to guess outcome of conditional branches
  - Static prediction: Based on instruction encoding
  - Dynamic prediction: Based on branch history
  - Reduces pipeline stalls

### Advanced CPU Features
- **SIMD Instructions**: Perform same operation on multiple data items
  - Examples: SSE, AVX, NEON
  - Used for multimedia, scientific computing
- **Speculative Execution**: Execute instructions before knowing if they're needed
  - Can lead to security vulnerabilities (Spectre, Meltdown)
- **Hyperthreading/SMT**: Multiple logical processors on a single physical core
  - Shares execution resources
  - Improves throughput for multi-threaded workloads
