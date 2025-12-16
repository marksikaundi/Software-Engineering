# Module 4: Storage and File Systems

## 1. File Systems

A file system provides a mechanism for online storage and access to both data and programs residing on the secondary storage (disks). It provides an abstraction of files and directories to the user, hiding the physical details of how data is stored.

**Key Responsibilities:**
- **File Management:** Creating, deleting, reading, and writing files.
- **Directory Management:** Organizing files into a hierarchical structure.
- **Access Control:** Enforcing permissions to control which users can access which files.

## 2. File System Interface

- **File Concept:** A named collection of related information that is recorded on secondary storage.
- **Attributes:** Name, identifier, type, location, size, protection, timestamps.
- **Operations:** Create, write, read, reposition, delete, truncate.

## 3. Directory Structure

- **Single-Level Directory:** One directory for all files. Simple but leads to naming conflicts.
- **Two-Level Directory:** Each user has their own directory. Solves naming conflicts but makes sharing files difficult.
- **Tree-Structured Directory:** A hierarchical structure of directories within directories. This is the most common modern approach.

## 4. File System Implementation

### a. Allocation Methods
This refers to how disk blocks are allocated for files.
- **Contiguous Allocation:** Each file occupies a set of contiguous blocks on the disk. Fast access but suffers from external fragmentation.
- **Linked Allocation:** Each file is a linked list of disk blocks. Solves fragmentation but does not support efficient random access.
- **Indexed Allocation:** Brings all the pointers for a file's blocks together into one location: the **index block**. Supports random access without external fragmentation, but the index block itself can be a bottleneck.

### b. Free-Space Management
The system must keep track of which blocks are free.
- **Bit Vector:** A map where each bit represents a disk block. `1` means allocated, `0` means free.
- **Linked List:** All free blocks are linked together.
