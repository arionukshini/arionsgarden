---
{"dg-publish":true,"permalink":"/semester-5/sisteme-operative/my-notes/","dg-note-properties":{}}
---

# My Notes

An **interrupt** is a signal that tells the CPU that an event needs immediate attention. 
It temporarily interrupts the currently running program so the OS can handle the event. 

How it works:
1. A program is running on the CPU. 
2. A device or software generates an interrupt. 
3. The CPU temporarily stops the current execution.
4. The CPU saves the current execution state. 
5. The OS identifies the interrupt. 
6. The appropriate Interrupt Service Routine (ISR) is executed. 
7. The interrupt is handled. 
8. The CPU restores the previous state and continues the interrupted program.

Type of Interrupts

![Pasted image 20261109131254.png](/img/user/Pasted%20image%2020261109131254.png)

A **clustered system** is a group of two or more computers (nodes) that work together and are connected through a network to provide services as a coordinated system.

To support this distinction in process requirements, most CPUs support two modes of operation: 
- user mode 
- kernel mode

### User Mode
The system is in user mode when the OS is running a user application such as handling a text editor. 
The transition from user mode to kernel mode occurs when the application requests the help of OS or an interrupt or a system call occurs. 
The mode bit is set to 1 in the user mode. It is changed from 1 to 0 when switching from user mode to kernel mode.
![Pasted image 20261109133456.png](/img/user/Pasted%20image%2020261109133456.png)

### Kernel Mode (supervisor mode, system mode, or privileged mode)

The system starts in kernel mode when it boots and after the OS is loaded, it executes applications in user mode. 
There are some privileged instructions that can only be executed in kernel mode.
	→ These are interrupt instructions, input/output management, etc. 
 Whenever the OS gains control of the computer, it is in kernel mode. 
If the privileged instructions are executed in user mode, it is illegal, and a trap is generated.


**Free software** (sometimes referred to as free/libre software) not only makes source code available but also is licensed to allow no-cost use, redistribution, and modification. 

**Open-source software** does not necessarily offer such licensing. Thus, although all free software is open source, some open-source software is not “free”. 
	Free software and open-source software are two different ideas championed by different groups of people.

### One set of OS services provides functions that are helpful to the user:

User Interface
Program execution
I/O operations
File-system manipulation
Communications
Error detection

### Another set of OS services exists for ensuring the efficient operation of the system itself via resource sharing:

Resource allocation
Logging/Accounting
Protection and security


**Why do you need system calls in OS?**
There are various situations where you must require system calls in the OS. Following of the situations are: 
- It is must require when a file system wants to create or delete a file. 
- If you want to read or write a file. 
- Network connections require the system calls to sending and receiving data packets. 
- If you want to access hardware devices, including a printer, scanner, etc. 
- To create and manage new processes.

## OS Design

### Design goals

User goals and System goals: 
- User goals – OS should be convenient to use, easy to learn, reliable, safe, and fast. 
- System goals – OS should be easy to design, implement, and maintain, as well as flexible, reliable, error-free, and efficient.

Early OSes were written in assembly language. 
- Now, most are written in higher-level languages such as C or C++, with small amounts of the system written in assembly language. 
- The lowest levels of the kernel might be written in assembly language and C. 
- Higher-level routines might be written in C and C++, and system libraries might be written in C++ or even higher-level languages.

### Simple Structure

![Pasted image 20261110094417.png](/img/user/Pasted%20image%2020261110094417.png)

### Monolithic Structure

Monolithic Structure is an OS architecture in which most OS services run together within a single large kernel in kernel mode. 
The kernel acts as a manager by managing all things like file management, memory management, devices management, and operational processes.
![Pasted image 20261110132024.png](/img/user/Pasted%20image%2020261110132024.png)

## System Boot

On most systems, the boot process proceeds as follows:
1. A small piece of code known as the bootstrap program or boot loader - BIOS (stored in ROM or EEPROM) locates the kernel. 
2. The kernel is loaded into memory and started.
3. The kernel initializes hardware.
4. The root file system is mounted. 

Modern systems replace BIOS with Unified Extensible Firmware Interface (UEFI). 
	UEFI has several advantages over BIOS, including better support for 64-bit systems and larger disks. 
GRUB is an open-source bootstrap program for Linux and UNIX systems.

The term ‘process’ is different from the terms: ‘job’ or ‘program’.
A program in execution is called a process!!!

### Process definition

Components of a process in OS: 
- Text/code section (instructions) - contains the program instructions to be executed. 
- Data section - the global and static variables initialized before execution begins. 
- Heap section - containing memory dynamically allocated during execution. 
- Stack section - stores local variables, function parameters, and return addresses.


### Process States

As a process executes, it changes state: 
- New: The process is being created 
- Ready: The process is waiting to be assigned to a processor 
- Running: Instructions are being executed 
- Waiting: The process is waiting for some event to occur
- Terminated: The process has finished execution
![Pasted image 20261110145806.png](/img/user/Pasted%20image%2020261110145806.png)

### Process Control Block (PCB)

A Process Control Block (PCB) is a data structure maintained by the OS that stores all essential information about a process. 
	→ Also called Task Control Block.

- Process ID (PID) - A unique identifier assigned to each process. 
- Process state – running, waiting, etc. 
- Program counter – location of instruction to next execute. 
- CPU registers – various CPU registers where process need to be stored for execution for running state. 
- CPU scheduling information- priorities, scheduling queue pointers. 
- Memory management information – memory allocated to the process. 
- Accounting information – CPU used, time limits, number of jobs or processes, etc. 
- I/O status information – I/O devices allocated to the process.

The processes are implemented by the means of process tables. 
The process tables store the ID of every process and, corresponding to it, the pointer to its PCB.
![Pasted image 20261110150604.png](/img/user/Pasted%20image%2020261110150604.png)

A **context switch** occurs when the CPU switches from one process to another.

Context switching happens in the following scenarios: 
- **Multitasking:** Switching between multiple processes to share CPU time. 
- **Interrupt handling:** When an interrupt occurs (e.g., I/O request or hardware signal), the OS saves the current process state and handles the interrupt. 
- **User and kernel mode switching:** When a process requests a system call, the OS switches from user mode to kernel mode.

### Schedulers

**Long-term Scheduler (Job Scheduler)** 
- Controls which processes are admitted from the job pool (disk) into main memory.
	→ This type of scheduling does not happen very frequently because a process needs some time in the system to be executed. 
**Short-term Scheduler (CPU Scheduler)** 
- Selects a process from the ready queue to execute on the CPU. 
	→ A process may execute for only a few milliseconds before waiting for an I/O request. 
**Medium-term Scheduler (Swapper)** 
- This scheduler is invoked when there is a need to swap out processes from memory to disk (i.e., suspend them) and later swap them back in based on factors such as memory pressure and process priority.

The **dispatcher** is a component of the CPU scheduler responsible for switching the CPU from one process to another.

Process identified and managed via a process identifier (pid), which is typically an integer number.

**UNIX/Linux:**
fork(): Creates a child process. 
exec(): Replaces the child process memory with a new program. 
wait(): Parent process wait for the child process to terminate.
![Pasted image 20261110154332.png](/img/user/Pasted%20image%2020261110154332.png)

**Windows:** CreateProcess(): Creates a new process.

A **zombie** process is a process that has completed execution (via the exit system call) but its parent has not read its exit status.
A process whose parent process has terminated without waiting - if a parent did not invoke wait() for its child process to terminate, is called an **orphan** process.
![Pasted image 20261110160052.png](/img/user/Pasted%20image%2020261110160052.png)

## IPC

Two fundamental models of IPC: 
- Shared Memory 
- Message Passing

Other types of IPC mechanisms are: 
- Pipes 
- Semaphores 
- Signals 
- Sockets
- Remote procedure Calls (RPCs)

IPC using shared memory requires communicating processes to establish a region of shared memory. 
Processes can then exchange information by reading and writing data to the shared region.