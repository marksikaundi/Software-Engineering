# Module 6: System Security

## 1. The Security Problem

Security is about protecting the system and its resources from unauthorized access, use, disclosure, disruption, modification, or destruction. It must defend against both internal and external attacks.

**Security Goals:**
- **Confidentiality:** Data is only accessible to authorized users.
- **Integrity:** Data cannot be modified undetectably.
- **Availability:** Resources are accessible to authorized users when needed.

## 2. Security Threats

- **Malware:** Malicious software designed to disrupt computer operation, gather sensitive information, or gain access to private computer systems.
  - **Viruses:** Code that attaches itself to another program.
  - **Worms:** Self-replicating programs that spread across a network.
  - **Trojan Horses:** Malicious code disguised as a legitimate program.
- **Denial of Service (DoS):** An attack designed to make a machine or network resource unavailable to its intended users.
- **Phishing:** Attempting to acquire sensitive information such as usernames, passwords, and credit card details by masquerading as a trustworthy entity.

## 3. Protection Mechanisms

Protection is the set of mechanisms that control the access of programs, processes, or users to the resources defined by a computer system.

### a. Principle of Least Privilege
Programs, users, and systems should be given just enough privileges to perform their tasks and no more. This limits the damage that can be caused by a malicious or compromised entity.

### b. Access Control
Access control is about specifying which users or processes can access which resources in what manner.
- **Access Control Lists (ACLs):** A list associated with each object (e.g., a file) that specifies the access rights for each user or group. `(file, {user1: read, user2: read/write})`
- **Capabilities:** A list associated with each subject (e.g., a process) that specifies the objects and operations it is allowed to perform. `(process, {file1: read, device2: read/write})`

## 4. Basic Cryptography
Cryptography can be used to ensure confidentiality and integrity.
- **Symmetric Encryption:** The same key is used for both encryption and decryption. Fast but has the problem of secure key distribution.
- **Asymmetric Encryption:** Uses a pair of keys: a public key (for encryption) and a private key (for decryption). Solves the key distribution problem but is computationally slower.
