# XV Quiz (CSL 3030)

Welcome to the XV Quiz for CSL 3030 - Operating Systems!



## Instructions
- Answer the multiple-choice questions by selecting the correct option.
- For theoretical questions, provide concise and accurate explanations.
- Feel free to use this quiz for self-assessment or educational purposes.

## Multiple-Choice Questions

#### Question 1: Basics
1. What is XV6?
   - a. A programming language
   - b. A Unix-like operating system
   - c. A file system
   - d. An assembly language

#### Question 2: Architecture
2. XV6 is based on which earlier operating system?
   - a. Windows
   - b. Linux
   - c. BSD
   - d. DOS

#### Question 3: File System
3. Which file system is used in XV6?
   - a. FAT32
   - b. NTFS
   - c. ext4
   - d. simple

#### Question 4: System Calls
4. How are system calls implemented in XV6?
   - a. As functions in the C standard library
   - b. As interrupts
   - c. Through the command line
   - d. As external programs

#### Question 5: Processes
5. In XV6, what is the maximum number of processes that can run simultaneously?
   - a. 128
   - b. 256
   - c. 512
   - d. 1024

#### Question 6: Shell
6. What is the name of the shell used in XV6?
   - a. Bash
   - b. Zsh
   - c. Sh
   - d. Fish

#### Question 7: Scheduling
7. How does XV6 handle process scheduling?
   - a. Round-robin scheduling
   - b. Priority-based scheduling
   - c. First-Come-First-Serve (FCFS)
   - d. Random scheduling

#### Question 8: Memory Management
8. Which memory management technique is used in XV6?
   - a. Paging
   - b. Segmentation
   - c. Virtual Memory
   - d. None of the above

#### Question 9: Interrupts
9. How are interrupts handled in XV6?
   - a. Through polling
   - b. Using hardware interrupts
   - c. Using software interrupts
   - d. Both b and c

#### Question 10: Multithreading
10. Does XV6 support multithreading?
    - a. Yes
    - b. No

#### Bonus Question:
11. Who developed XV6?
    - a. Microsoft
    - b. Google
    - c. MIT
    - d. IBM

## Theoretical Questions

#### Question 12: Process States
12. Briefly explain the different states a process can be in within the XV6 operating system.

#### Question 13: File System Structure
13. Describe the structure of the file system in XV6. Include the key components and their roles.

#### Question 14: System Calls vs. Library Functions
14. Explain the difference between system calls and library functions in the context of XV6. Provide examples of each.

#### Question 15: Memory Paging
15. How does memory paging work in XV6? Discuss the benefits of using paging in memory management.

#### Question 16: Shell Commands
16. Name and briefly explain three essential shell commands in the XV6 operating system.

#### Question 17: Process Synchronization
17. Discuss the concept of process synchronization in XV6. Why is it essential, and what mechanisms are used to achieve it?

#### Question 18: Interrupt Handling
18. Explain the role of interrupts in the XV6 operating system. How are interrupts handled, and what is their significance in system operation?

#### Question 19: Virtual Memory
19. What is virtual memory, and how is it implemented in XV6? Discuss the advantages of using virtual memory.

#### Question 20: Boot Process
20. Outline the steps involved in the boot process of XV6. What happens from the moment the computer is powered on to when the XV6 kernel is loaded into memory?

## Answers

1. (b) A Unix-like operating system
2. (c) BSD
3. (d) simple
4. (b) As interrupts
5. (c) 512
6. (c) Sh
7. (a) Round-robin scheduling
8. (a) Paging
9. (d) Both b and c
10. (b) No
11. (c) MIT
12. Running - the process is currently executing
    Sleeping - the process is not running, waiting for an event
    Zombie - the process has finished executing but still has an entry in the process table
    Unused - the process table entry is empty/available
    Runnable -
    

13. Superblock - contains metadata like size and free blocks
    Inode blocks - map file names to disk blocks
    Data blocks - contain file data This simple structure allows basic file manipulation like creating, deleting, opening files.

14. System calls provide the interface between user processes and the kernel. Examples are read, write, open, close. Library functions are part of the C standard library that applications can link to - printf, malloc, string functions.

15. Paging in XV6 involves dividing physical memory into fixed-size blocks called pages. These pages are used to manage virtual memory, providing several benefits like efficient use of memory, easier memory allocation, and protection between different processes' memory spaces.

16. ls: shows directory contents.
    cd: Changes the current directory.
    mkdir: make directories

17. Process synchronization ensures predictable execution using primitives like locks and semaphores. This prevents race conditions. XV6 uses simple locking allowing only one process to enter critical sections.

18. Interrupts trigger the processor to suspend current execution and run an interrupt handler. This allows implementing I/O device drivers and low-level functionality. XV6 handles interrupts via the intr() function and interrupt descriptor table.

19. Virtual memory uses paging and swapping to give each process the illusion of a large, contiguous address space. It provides isolation between processes. XV6 does not implement virtual memory. All processes access the same physical memory.

20.
The boot steps are:
Execute bootloader from ROM
Load kernel image from disk to memory
Set up interrupt descriptor table
Call main() in kernel - initializes subsystems
Create first process - init proc
init proc exec's the user shell
