# Module 1: Introduction to Operating Systems

## 1. What is an Operating System?

An Operating System (OS) is system software that acts as an intermediary between the computer hardware and the user. Its primary goals are to:
- **Manage Hardware Resources:** Allocate and manage resources like the CPU, memory, and I/O devices efficiently and fairly.
- **Provide a User Interface:** Offer a platform for users to interact with the computer (e.g., Command-Line Interface (CLI) or Graphical User Interface (GUI)).
- **Execute and Provide Services for Programs:** Create an environment where user programs can run and access necessary resources.

## 2. Key Functions of an OS

- **Process Management:** Manages the lifecycle of processes and threads.
- **Memory Management:** Allocates and deallocates memory space as required.
- **File System Management:** Organizes files and directories on storage devices.
- **I/O Management:** Handles communication with input/output devices.
- **Security and Protection:** Ensures system integrity and protects resources from unauthorized access.

## 3. Structure of an Operating System

### a. Monolithic Kernel
The entire OS runs as a single large process in kernel space. It's fast but less modular and harder to maintain.
- **Examples:** Early versions of Linux, MS-DOS.

### b. Microkernel
The kernel is broken down into smaller, separate processes called "servers." Only the most fundamental functions reside in the kernel (e.g., IPC, basic memory management).
- **Advantages:** More secure, reliable, and easier to extend.
- **Disadvantages:** Higher overhead due to frequent message passing between servers.
- **Examples:** GNU Hurd, QNX.

### c. Hybrid Kernel
A combination of monolithic and microkernel designs. It keeps more services in the kernel than a microkernel to improve performance but retains some modularity.
- **Examples:** Modern Windows (NT Kernel), macOS (XNU Kernel), and Linux.

## 4. System Calls

A system call is the programmatic way a user-level process requests a service from the kernel. When a program needs to perform a privileged action (e.g., reading a file, opening a network connection), it cannot do so directly. Instead, it must trap into the kernel via a system call, which then performs the action on its behalf and returns the result.
