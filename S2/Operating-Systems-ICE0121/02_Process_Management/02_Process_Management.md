# Module 2: Process Management

## 1. What is a Process?

A process is an instance of a computer program that is being executed. It is more than just the program code; it is a dynamic entity that includes:
- **Program Counter:** The address of the next instruction to execute.
- **CPU Registers:** The current state of the processor.
- **Process Stack:** Contains temporary data such as function parameters, return addresses, and local variables.
- **Data Section:** Contains global variables.
- **Heap:** Memory that is dynamically allocated during runtime.

Each process is an independent entity with its own address space.

## 2. Process States

A process transitions between several states during its lifecycle:
- **New:** The process is being created.
- **Running:** Instructions are being executed by the CPU.
- **Waiting:** The process is waiting for some event to occur (e.g., I/O completion).
- **Ready:** The process is waiting to be assigned to a processor.
- **Terminated:** The process has finished execution.

## 3. CPU Scheduling

CPU scheduling is the basis of multiprogramming. By switching the CPU among processes, the OS can make the computer more productive. The **scheduler** selects a process from the ready queue to run.

### Common Scheduling Algorithms:
- **First-Come, First-Served (FCFS):** Simple but can lead to long average waiting times.
- **Shortest-Job-First (SJF):** Optimal in terms of average waiting time, but predicting the future execution time is difficult. Can be preemptive or non-preemptive.
- **Priority Scheduling:** Each process has a priority, and the CPU is allocated to the process with the highest priority. Can lead to starvation of low-priority processes.
- **Round Robin (RR):** Each process gets a small unit of CPU time (time quantum). It's fair and provides good response times for interactive systems.

## 4. Inter-Process Communication (IPC)

IPC provides a mechanism for cooperating processes to communicate and synchronize their actions. The two main models are:

### a. Shared Memory
A region of memory is shared between processes. Communication is fast, but it is the responsibility of the application developer to ensure synchronization and avoid conflicts.

### b. Message Passing
Processes communicate by exchanging messages. The OS provides system calls for sending and receiving messages, which simplifies development but incurs more overhead than shared memory.
