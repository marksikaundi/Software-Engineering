# Resource: Key Concepts Summary

### Module 1: Introduction
- The OS acts as an intermediary between the user and the hardware.
- Core functions: Process, memory, file system, and I/O management.
- Kernel Architectures: Monolithic (fast, less modular), Microkernel (modular, more overhead), Hybrid (balanced approach).
- **System Calls** are the bridge between user processes and the kernel.

### Module 2: Process Management
- A **process** is a program in execution, with its own address space.
- Process states: New, Running, Waiting, Ready, Terminated.
- **CPU Scheduling** manages which process runs on the CPU. Key algorithms: FCFS, SJF, Priority, Round Robin.
- **IPC** (Inter-Process Communication) allows processes to cooperate via Shared Memory or Message Passing.

### Module 3: Memory Management
- Manages main memory to improve utilization.
- Paging avoids external fragmentation by dividing memory into fixed-size **pages** and **frames**.
- **Virtual Memory** allows programs to be larger than physical memory by using disk space as an extension of RAM.
- **Page Replacement Algorithms** (like FIFO, LRU) decide which page to evict from memory when a new page is needed.

### Module 4: Storage and File Systems
- A **file system** provides a logical view of storage, organizing data into files and directories.
- **Allocation Methods** (Contiguous, Linked, Indexed) determine how files are stored on disk.
- Free space is managed using techniques like bit vectors or linked lists.

### Module 5: Concurrency
- Concurrency issues arise when multiple processes share data.
- The **Critical Section** is the part of the code that accesses shared data.
- **Mutual Exclusion** ensures only one process can be in its critical section at a time.
- Synchronization tools like **Mutexes** and **Semaphores** are used to enforce mutual exclusion and prevent race conditions.

### Module 6: System Security
- **Protection** involves mechanisms to control access to resources.
- The **Principle of Least Privilege** is a fundamental security design principle.
- Access control can be implemented using **Access Control Lists (ACLs)** or **Capabilities**.
- Threats include malware and DoS attacks. Cryptography helps ensure confidentiality and integrity.
