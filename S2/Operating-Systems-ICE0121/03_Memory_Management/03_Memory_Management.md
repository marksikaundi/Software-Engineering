# Module 3: Memory Management

## 1. Introduction

Memory management is the function of an OS responsible for managing the computer's primary memory. It keeps track of each memory location, decides which processes get memory, when they get it, and how much they get.

## 2. Memory Allocation Techniques

### a. Contiguous Allocation
Each process is contained in a single contiguous section of memory.
- **Fixed-Partitioning:** Memory is divided into fixed-size partitions. Simple but suffers from **internal fragmentation** (wasted space within a partition).
- **Variable-Partitioning:** Partitions are created dynamically to fit the needs of each process. Solves internal fragmentation but suffers from **external fragmentation** (memory is available but not contiguous, so it cannot be used).

### b. Paging
The most common memory management technique.
- **Physical Memory** is divided into fixed-size blocks called **frames**.
- **Logical Memory** (the process's address space) is divided into fixed-size blocks called **pages**.
- The OS maintains a **Page Table** for each process, which maps pages to frames.
- Paging allows a process's physical address space to be non-contiguous, completely solving the problem of external fragmentation.

## 3. Virtual Memory

Virtual memory is a technique that allows the execution of processes that are not completely in memory. It creates the illusion that each process has its own contiguous address space, separate from all other processes.

**Key Benefits:**
- Allows programs to be larger than physical memory.
- Increases the degree of multiprogramming because less of each process needs to be in memory.
- Simplifies memory management for programmers.

### Demand Paging
Pages are loaded from the disk into memory only when they are needed (demanded). This is the most common implementation of virtual memory.

### Page Replacement Algorithms
When a new page needs to be loaded and there are no free frames, the OS must decide which page in memory to swap out to disk.
- **FIFO (First-In, First-Out):** Replaces the oldest page. Simple but can perform poorly.
- **Optimal (OPT):** Replaces the page that will not be used for the longest period of time. Unimplementable in practice but serves as a benchmark.
- **LRU (Least Recently Used):** Replaces the page that has not been used for the longest period of time. A good approximation of OPT and commonly used.
