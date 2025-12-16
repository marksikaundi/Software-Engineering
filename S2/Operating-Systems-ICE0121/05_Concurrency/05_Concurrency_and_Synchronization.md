# Module 5: Concurrency and Synchronization

## 1. The Challenge of Concurrency

Concurrency is the execution of multiple instruction sequences at the same time. In an OS, this happens when multiple processes or threads are running "in parallel". While true parallelism only occurs on multi-core systems, a single-core system creates the illusion of parallelism through rapid context switching.

**The core problem:** When multiple processes access and manipulate the same shared data, the final result can depend on the specific order in which their instructions are interleaved. This is called a **race condition**.

## 2. The Critical Section Problem

The part of a program where shared resources are accessed is called the **critical section**. To prevent race conditions, we must ensure that only one process can be executing in its critical section at a time. This property is called **mutual exclusion**.

A solution to the critical section problem must satisfy three requirements:
1.  **Mutual Exclusion:** Only one process at a time can be in its critical section.
2.  **Progress:** If no process is in a critical section, and some processes want to enter, only those not in their remainder sections can participate in the decision of which will enter next, and this selection cannot be postponed indefinitely.
3.  **Bounded Waiting:** There must be a limit on the number of times that other processes are allowed to enter their critical sections after a process has made a request to enter its critical section and before that request is granted.

## 3. Synchronization Primitives

These are tools provided by the OS to help solve the critical section problem.

### a. Mutex Locks (Mutual Exclusion)
A mutex is the simplest synchronization tool. It's a lock that a process must acquire before entering a critical section and release when it exits. If the lock is already held by another process, the requesting process will be blocked until the lock is released.

### b. Semaphores
A semaphore is a more sophisticated tool. It's an integer variable that, apart from initialization, is accessed only through two standard atomic operations: `wait()` and `signal()`.

- **`wait(S)`:** Decrements the semaphore value. If the value becomes negative, the process blocks.
- **`signal(S)`:** Increments the semaphore value. If the value is not positive, a waiting process is unblocked.

Semaphores can be used to control access to a resource with a limited number of instances (a **counting semaphore**) or to enforce mutual exclusion (a **binary semaphore**, which is functionally equivalent to a mutex).
