# Resource: Practice Questions

### Module 1: Introduction
1.  What are the two primary goals of an operating system?
2.  Explain the difference between a monolithic kernel and a microkernel. What are the advantages of each?
3.  Why are system calls necessary? Why can't user programs perform privileged operations directly?

### Module 2: Process Management
1.  What is the difference between a process and a program?
2.  Consider the FCFS, SJF, and Round Robin scheduling algorithms. Which one would you choose for an interactive system where user responsiveness is critical? Why?
3.  What are the pros and cons of using shared memory for IPC versus message passing?

### Module 3: Memory Management
1.  Explain the difference between internal and external fragmentation. Which memory allocation schemes suffer from each?
2.  How does virtual memory allow a program to be larger than the physical RAM?
3.  A system has 3 page frames. For the reference string `1, 2, 3, 4, 1, 2, 5, 1, 2, 3, 4, 5`, how many page faults would occur for the LRU and FIFO replacement algorithms?

### Module 4: Storage and File Systems
1.  Compare contiguous, linked, and indexed file allocation methods. What are their main trade-offs?
2.  What is the purpose of a directory in a file system?
3.  Why is random access slow with linked allocation?

### Module 5: Concurrency
1.  Define "race condition." Provide a simple pseudo-code example of a race condition.
2.  What is the "critical section problem," and what three conditions must a solution satisfy?
3.  What is the difference between a mutex and a semaphore? When would you use one over the other?

### Module 6: System Security
1.  Explain the "Principle of Least Privilege."
2.  What is the difference between an Access Control List (ACL) and a Capability List?
3.  Why is symmetric encryption faster than asymmetric encryption? What problem does asymmetric encryption solve?
