---
{"dg-publish":true,"permalink":"/semester-5/sisteme-operative/notes-gpt/","tags":["universitet","semestri-5","sisteme-operative"],"dg-note-properties":{"tags":["universitet","semestri-5","sisteme-operative"]}}
---

# Operating Systems

## Introduction

An **Operating System (OS)** is an intermediary between users and computer hardware.  
Its purpose is to provide an environment in which users can execute programs in a convenient and efficient manner.

The OS manages the computer's hardware and provides an environment in which other programs can do useful work.

**User view:** convenience, ease of use, and good performance.  
**System view:** efficient use of hardware and management of program execution.

The OS is a:

- **Resource allocator** - decides how CPU time, memory, storage, and devices are shared.
- **Control program** - controls the execution of programs and the use of hardware.

The **kernel** is the central part of the OS that runs with full privileges.  
System programs are supplied with the OS but are not part of the kernel.  
Application programs perform the user's tasks.

**Middleware** is a set of software frameworks that provides additional services to application developers, such as databases, multimedia, and graphics.

A program passes through these levels:

Application → Libraries and utilities → Operating system → Hardware

The compiler produces an executable. The OS creates a process, allocates RAM, schedules CPU time, and manages I/O. The CPU executes instructions, RAM holds working data, and storage keeps saved files.

### History

- First generation (1945-1955): Vacuum tubes.
- Second generation (1955-1965): Transistors and batch systems.
- Third generation (1965-1980): Integrated circuits and multiprogramming.
- Fourth generation (1980-present): Personal computers.
- Fifth generation (1990-present): Mobile computers.

### Types of Operating Systems

**Mainframe OS** processes many jobs at once, usually with large amounts of I/O.  
Services: batch processing, transaction processing, and timesharing.

**Server OS** serves multiple users over a network and allows them to share hardware and software resources.

**Multiprocessor OS** uses more than one CPU to improve performance. Work can be divided among processors.

**Personal computer OS** supports multiprogramming and multiprocessor architectures.

**Smartphone and handheld OS** runs on portable devices such as smartphones and tablets. Mobile devices have limited resources and must consider usability and battery life.

**IoT OS** runs on small computers in network-connected objects containing sensors and actuators.

**Embedded OS** is designed for a specific purpose. It is small, resource-efficient, and dependable, with features limited to what the application needs.  
→ Examples: car engines, industrial robots, microwave ovens, and medical devices. Many work without direct user interaction.

**Real-Time OS (RTOS)** has well-defined time constraints. Processing must finish within the required time.

- Hard real time: missing a deadline is a system failure.
- Soft real time: missing a deadline reduces service quality.
- Firm real time: a late result has no value.

**Smart-card OS** operates with very limited memory and processing power.

### Computer-System Organization

Main components:

- Processors: CPU and GPU.
- Memory: RAM, ROM, and cache.
- Nonvolatile storage: HDD, SSD, and persistent memory.
- I/O devices and their controllers.
- Buses/interconnects: PCIe, PCI, USB, SATA, and DMI.

### Interrupts

An **interrupt** is a signal that tells the CPU that an event needs attention.  
It temporarily interrupts the currently running program so the OS can handle the event.

How it works:
1. A program is running on the CPU.
2. A device or software generates an interrupt.
3. The CPU temporarily stops the current execution.
4. The execution state is saved.
5. The OS identifies the interrupt.
6. The appropriate Interrupt Service Routine (ISR) executes.
7. The interrupt is handled.
8. The saved state is restored and execution can continue.

Types of interrupts:

![Pasted image 20261109131254.png](/img/user/Pasted%20image%2020261109131254.png)

An OS is **interrupt driven**.

A hardware interrupt comes from a device. A trap/exception is associated with executing software, such as an error or a request for an OS service.  
→ Keyboard input generates a hardware interrupt. Interrupts and traps can occur while a user application is running.

### Storage

**Main memory (RAM)** holds the instructions and data currently being used. The CPU can access it directly.  
**Secondary storage** provides larger, nonvolatile storage capacity.

- HDD: magnetic recording on rotating platters.
- SSD: flash memory, faster than a traditional HDD.
- NVM: nonvolatile memory that retains data without power.

**Volatile** memory loses its contents without power.  
**Nonvolatile** storage retains its contents.

Storage hierarchy, from faster/smaller to slower/larger:

Registers → Cache → Main memory → Nonvolatile memory → HDD → Optical disk → Magnetic tape

In **von Neumann architecture**, instructions and data are stored together in the same main memory and processed by the same CPU.

### Computer-System Architecture

A **single-processor system** has one general-purpose processor, but may also contain special-purpose processors.

A **multiprocessor system**, also called a parallel system, uses multiple processors.

Advantages:

- Increased throughput.
- Economy of scale through shared resources.
- Increased reliability and fault tolerance.

**Asymmetric multiprocessing:** each processor is assigned a specific task.  
**Symmetric multiprocessing (SMP):** processors can perform the same general tasks and share main memory.

- CPU: hardware that executes instructions.
- Processor: a physical chip containing processing hardware.
- Core: a basic computation unit.
- Multicore: multiple cores on one chip.
- Multiprocessor: multiple processors.

**Blade servers** place multiple processor boards, I/O boards, and networking boards in the same chassis.

### Clustered Systems

A **clustered system** is a group of two or more computers (nodes) that work together and are connected through a network to provide services as a coordinated system.  
They usually share storage through a **Storage-Area Network (SAN)**.

Clusters can provide high availability, load balancing, and continued service when a node fails.

- Asymmetric clustering: one machine is in hot-standby mode.
- Symmetric clustering: several nodes run applications and monitor one another.

Some clusters are used for **High-Performance Computing (HPC)**.  
→ Applications must be written to use parallelization.

### Multiprogramming and Multitasking

**Multiprogramming** keeps multiple programs in main memory at the same time, allowing the CPU to switch between them.

- The goal is to maximize CPU utilization.

**Timesharing**, also called **multitasking**, allows processes to share the CPU by giving each one a small amount of CPU time.

- The goal is fast response and interactive use.

## OS Functions

### User Mode

The system is in **user mode** when it runs an ordinary user application, such as a text editor. Applications have restricted access to memory and I/O devices.

A system call, interrupt, or exception can transfer control to the kernel.  
The mode bit is **1 in user mode** and changes to **0 in kernel mode** in this model.

![Pasted image 20261109133456.png](/img/user/Pasted%20image%2020261109133456.png)

### Kernel Mode

Also called **supervisor mode, system mode, or privileged mode**.

The system starts with privileged execution during boot. Once the OS is ready, ordinary applications run in user mode.

Privileged instructions can only execute in kernel mode.  
→ Examples include controlling interrupts and managing I/O hardware.

Attempting a privileged instruction in user mode generates a trap.

Some systems support additional modes, such as a Virtual Machine Manager (VMM) mode for virtualization.

### Process Management

A **process** is a program in execution. It needs CPU time, memory, I/O, files, and initialization data.

A single-threaded process has one program counter.  
A multithreaded process has one program counter per thread.

The OS is responsible for:

- Creating and deleting user and system processes.
- Scheduling processes and threads on CPUs.
- Suspending and resuming processes.
- Providing synchronization and communication mechanisms.
- Providing mechanisms for deadlock handling.

### Memory Management

Memory management controls and coordinates the use of main memory (RAM).  
All or part of a program's instructions must be in memory before it can execute.

The OS:

- Keeps track of which parts of memory are used and by which processes.
- Decides which processes and data move into and out of memory.
- Allocates and deallocates memory as needed.

### File-System Management

File-system management organizes, stores, accesses, and protects files and directories. Files are usually organized into directories.

Activities:

- Create and delete files and directories.
- Organize directories.
- Manage file access and permissions.
- Map files onto secondary storage.
- Back up files.
- Provide protection and sharing.

### Device and Mass-Storage Management

The OS controls hardware devices and manages persistent storage such as HDDs and SSDs.

Activities:

- Communicate with devices through device drivers.
- Handle I/O operations between applications and hardware.
- Allocate and deallocate storage.
- Manage free space.
- Schedule disk operations.
- Control device access.

### Cache Management

**Cache management** stores frequently or recently accessed data in faster memory so it can be accessed more quickly.

The cache is checked first:

- If the information is present, it is used directly.
- Otherwise, it is fetched from slower storage and may be copied into cache.

### I/O System Management

The OS manages input/output operations between the computer and external devices.

- Input: keyboard, mouse, sensors.
- Output: display, printer, speakers.
- Device drivers, I/O requests, and device protection.

**Buffering** temporarily holds data during a transfer.  
**Caching** keeps a copy for faster reuse.  
**Spooling** queues work for a device, such as print jobs.

### Protection and Security

**Protection** controls how processes and users access resources such as memory, files, CPU, and devices.

**Security** protects the system and data against unauthorized access, attacks, and misuse.

- Authentication: verifies identity.
- Authorization: determines what the user/process may access.
- Access control: enforces permissions and policies.

### Virtualization

**Virtualization** represents physical resources as one or more virtual resources. Multiple isolated environments can share the same hardware.

A physical server can run several **Virtual Machines (VMs)**, each with its own OS and applications.  
A **hypervisor**, or **VMM**, manages and allocates the hardware resources among the VMs.

### Kernel Data Structures

An **array** stores elements that can be accessed directly by index.

A **linked list** stores items connected to one another.

- Singly linked: each item points to its successor.
- Doubly linked: each item points to its predecessor and successor.
- Circular: the last item points to the first instead of null.

A **stack** uses **LIFO** (Last In, First Out).  
→ Insert with `push`, remove with `pop`.

A **queue** uses **FIFO** (First In, First Out).  
→ Items are removed in the order they were inserted.

A **tree** represents data hierarchically through parent-child relationships.  
A binary-tree node has at most two children.

A **hash function** converts a key into a numeric hash used to locate data in a table.  
A **hash map** uses hashing to store and retrieve key-value pairs efficiently.

A **bitmap** uses `n` bits to represent the status of `n` items.  
→ For example, a bit can indicate whether a resource is free or allocated. It is space-efficient.

### Distributed Systems

A **distributed system** is a collection of independent networked computers that cooperate and appear to users as a single coherent system.

Key characteristics:

- Resource sharing: data, services, and processing resources.
- Concurrency: components operate simultaneously.
- Communication: nodes communicate over a network.
- Scalability: resources can be added as demand increases.
- Fault tolerance: operation can continue despite some failures.

### Client-Server Systems

In a **client-server system**, clients request services or resources and servers process the requests and return responses.

- Client: initiates requests and provides the user interface/application.
- Server: provides services and manages shared resources.
- Communication usually uses a network, with protocols such as TCP/IP, HTTP, or HTTPS.
- Multiple clients can access the same server resources.

### Peer-to-Peer Systems

In a **Peer-to-Peer (P2P)** system, each participant (peer) can act as both client and server. Resources, data, and processing power are distributed across nodes.

Examples: BitTorrent, blockchain, and Skype's original P2P model.

### Cloud Computing

**Cloud computing** delivers computing resources over the internet, such as servers, storage, databases, networking, and software.

### Free and Open-Source Software

**Free/libre software** grants the freedom to use, study, modify, and redistribute the software.  
→ “Free” refers to freedom, not necessarily zero price.

**Open-source software** makes source code available under a licence allowing use, modification, and redistribution. Free software and open source emphasize different ideas, but largely overlap.

- GNU/Linux: open-source OS family.
- Windows: proprietary OS.
- macOS: combines open and proprietary components. Darwin is the open-source foundation; XNU is its kernel.

## OS Services

OS services provide an environment for program execution and support programs and users.

### Services Helpful to the User

- **User interface:** interaction through CLI, GUI, or touchscreens.
- **Program execution:** load a program into memory, execute it, and terminate it.
- **I/O operations:** access files and I/O devices.
- **File-system manipulation:** read, write, create, delete, search, list information, and manage permissions.
- **Communications:** exchange data locally or over a network, using shared memory or message passing.
- **Error detection:** detect and handle errors in hardware, programs, memory, and I/O.

Examples of errors: memory errors, power failure, network failure, no paper in a printer, arithmetic overflow, and illegal memory access.

### Services for Efficient System Operation

- **Resource allocation:** distribute CPU time, memory, storage, and devices among users/processes.
- **Logging/accounting:** track CPU time, memory, disk usage, and other resource use.
- **Protection and security:** control access, authenticate users, and prevent unauthorized use.

### User Interfaces

A **Command-Line Interface (CLI)** accepts commands from the user and executes them. The command interpreter may be a system program or part of the kernel.

A **shell** is a command interpreter.  
→ Bourne shell is a Unix shell.

A **Graphical User Interface (GUI)** uses windows, icons, menus, buttons, and mouse/touch interaction. Many OSes provide both CLI and GUI.

A **touchscreen interface** supports direct interaction through touch and gestures. Voice commands provide another input method.

### System Calls

**System calls** are the programming interface between user applications and the OS kernel. They allow programs to request services involving hardware and other system resources.

They are commonly available through C/C++ functions. Some low-level implementation uses assembly instructions.

Why system calls are needed:

- To create or delete a file.
- To read or write a file.
- To send and receive network data.
- To access hardware devices.
- To create and manage processes.

An **Application Programming Interface (API)** is the interface used by the programmer. An API operation may use one or several system calls, or none if it can complete in user space.

Common APIs:

- Win32 API for Windows.
- POSIX API for Unix-like systems, including Linux and macOS.
- Java API for the Java Virtual Machine (JVM).

### System-Call Implementation

A number is associated with each system call. The system-call interface maintains a table indexed by these numbers.

The interface invokes the intended kernel routine and returns its status and any result. The caller follows the API without needing to know the implementation.

User process running → Requests system call → Kernel executes the service → Returns to user mode with result

For example, `open()` goes through the system-call interface to the kernel's implementation and returns a file descriptor or an error.

To copy a file, as in `cp in.txt out.txt`:
1. Obtain the input and output file names.
2. Open the input and create the output.
3. Read from the input and write to the output repeatedly.
4. Close the files.
5. Report completion and terminate.

### Types of System Calls

- **Process control:** create, execute, and terminate processes.  
  → `fork()`, `exec()`, `exit()`.
- **File management:** open, read, write, and close files.  
  → `open()`, `read()`, `write()`, `close()`.
- **Device management:** request, configure, and release devices.  
  → `ioctl()`, `read()`, `write()`.
- **Memory management:** allocate and manage memory.  
  → `mmap()`, `munmap()`.
- **Communication:** exchange data between processes.  
  → `pipe()`, `socket()`, `send()`, `recv()`.
- **Protection/security:** control resource access.  
  → `chmod()`, `setuid()`, `access()`.

Windows and Unix interfaces for similar operations:

- Create process: `CreateProcess()` / `fork()`.
- Terminate: `ExitProcess()` / `exit()`.
- Wait: `WaitForSingleObject()` / `wait()`.
- Open/create file: `CreateFile()` / `open()`.
- Read/write: `ReadFile()`, `WriteFile()` / `read()`, `write()`.
- Close: `CloseHandle()` / `close()`.
- Device operations: console functions / `ioctl()`, `read()`, `write()`.
- Process ID: `GetCurrentProcessId()` / `getpid()`.
- Timer/sleep: `SetTimer()`, `Sleep()` / `alarm()`, `sleep()`.
- Pipes/shared memory: `CreatePipe()`, file-mapping functions / `pipe()`, `shm_open()`, `mmap()`.
- Protection: security-descriptor functions / `chmod()`, `umask()`, `chown()`.

### System Programs

System programs provide common functions for applications and users:

- File management: create, delete, copy, rename, print, and list files/directories.
- Status information: date, time, available memory, disk space, users, performance, and logs.
- File modification: text editors, searches, and text transformations.
- Programming-language support: compilers, assemblers, debuggers, and interpreters.
- Program loading and execution.
- Communication between processes, users, and computers.
- Background services.

Some systems use a **registry** to store configuration information.

**Background services** run without direct user interaction. They are also called services, subsystems, or daemons. They run as user-space programs and request kernel services when needed.

**Application programs** perform specific user tasks using OS services.  
→ Browsers, word processors, spreadsheets, databases, development tools, media players, statistical tools, and games.

### Linkers and Loaders

Source files are compiled into **relocatable object files**.  
The **linker** combines object files into a binary executable.  
The **loader** loads the executable into memory so it can run on a CPU core.

Source code → Object files → Linker → Executable → Loader → Memory

Applications are OS-specific because of differences in executable formats, system calls, and sometimes CPU instruction sets.

## OS Design

The first problem in designing an OS is to define its goals and specifications. The design depends on the hardware and the type of system: desktop, mobile, distributed, or real time.

### Design Goals

- **User goals:** convenient to use, easy to learn, reliable, safe, and fast.
- **System goals:** easy to design, implement, and maintain; flexible, reliable, error-free, and efficient.

**Policy:** What will be done?  
**Mechanism:** How will it be done?

Separating policy from mechanism makes it easier to change decisions without changing the underlying implementation.

Early OSes were written in assembly language.

- Most are now written in higher-level languages such as C/C++, with some assembly.
- The lowest kernel levels may use assembly and C.
- Higher-level routines and system libraries can use higher-level languages.

### Simple Structure

A simple structure is small and loosely organized. It has little separation between components and weak protection between applications and hardware.  
→ MS-DOS is an example.

![Pasted image 20261110094417.png](/img/user/Pasted%20image%2020261110094417.png)

Advantages:

- Easy to develop.
- Good performance.
- Minimal overhead.

Disadvantages:

- A program failure can crash the entire OS.
- Limited functionality.
- Does not enforce data hiding.

### Monolithic Structure

**Monolithic structure** is an OS architecture in which most OS services run together within a single large kernel in kernel mode.

The kernel manages files, memory, devices, and processes and serves as the main interface to hardware. Traditional UNIX consists of a kernel and system programs.

![Pasted image 20261110132024.png](/img/user/Pasted%20image%2020261110132024.png)

Advantages:

- Simple overall structure.
- Fast communication between components in the same kernel space.

Disadvantages:

- A faulty kernel service can crash the whole system.
- Difficult to extend or modify because components depend on one another.
- The kernel can become large and complex.

### Layered Structure

The OS is divided into layers. Hardware is at the bottom (**layer 0**) and the user interface is at the top. Higher layers use the functions of lower layers.

Advantages:

- Easier to understand, maintain, and extend.
- Each layer has a separate responsibility.
- Simpler construction and debugging.

Disadvantages:

- Communication between layers adds overhead.
- Dividing the system into suitable layers requires careful planning.

### Microkernel Structure

A **microkernel** keeps only essential functions in kernel mode. Other services run as separate programs in user space and communicate through **message passing**.

The kernel provides basic memory management, CPU scheduling, and IPC. Services such as file systems and device drivers can run in user space.

Advantages:

- Easier to extend and port to other platforms.
- Less code runs in kernel mode.
- Better isolation, reliability, and security.
- A failed user-space service can be isolated from the rest of the OS.

Disadvantages:

- Communication between user space and kernel space adds overhead.
- More complex to construct and coordinate.

### Modular Structure

The OS is divided into **independent modules**. Each module has a specific task, such as memory management, process scheduling, or device drivers.

Modules have clearly defined interfaces and can be **loaded and unloaded dynamically**.  
→ Loadable Kernel Modules (**LKMs**).

A module can be added during boot or runtime, such as when a USB device is connected. Modular designs are used in systems such as Linux, Solaris, macOS, and Windows.

Advantages:

- Easier to understand, develop, and maintain.
- Flexible: modules can be added, modified, or removed.

Disadvantages:

- Communication between modules can add overhead.
- Modules must be carefully designed to interact correctly.

### Hybrid-Kernel Structure

A **hybrid kernel** combines monolithic and microkernel ideas to balance performance, flexibility, and reliability. Most modern OSes do not use one pure model.

- Linux: monolithic kernel with dynamically loadable modules.
- Windows: substantial kernel components, user-mode subsystems, and loadable kernel components.
- macOS/iOS: applications, user experience, application frameworks, core frameworks, and the Darwin kernel environment.
- Android: applications, runtime/frameworks, native libraries, hardware abstraction, and a Linux kernel.

Advantages:

- Good performance.
- Supports a wide range of hardware and applications.
- Can combine modularity with service isolation.

Disadvantages:

- Greater design complexity.
- IPC between kernel and user-space services can add overhead.

### Building an OS

1. Write the source code.
2. Configure the OS for the target system.
3. Compile it.
4. Install it.
5. Boot the computer with the new OS.

### System Boot

**Booting** is the process of starting the computer and loading the OS into memory.

1. Firmware begins execution at a fixed starting location.
2. Firmware and boot-loader code locate and load the kernel.
3. The kernel starts and initializes hardware.
4. The root file system is mounted.

Modern systems use **UEFI (Unified Extensible Firmware Interface)** instead of traditional **BIOS (Basic Input/Output System)**.  
UEFI supports newer architectures, faster booting, and larger storage configurations.

**GRUB** is an open-source boot loader used by Linux/Unix systems.

### Debugging and Performance

**OS debugging** identifies, analyzes, and fixes errors, bugs, and performance problems.

- Log file: records error information.
- Core dump: captures a failed application's process memory.
- Crash dump: captures kernel memory after an OS failure.

**Performance tuning** improves performance by removing bottlenecks.  
→ For example, identify and optimize a process that keeps CPU utilization near 100%.

Tools: `top` and Windows Task Manager.

## Processes

A **program** is a passive entity stored on disk as an executable file.  
A **process** is active: a program in execution.

### Process Definition

Components of a process:

- **Text/code section:** program instructions.
- **Data section:** global and static variables, including initialized and uninitialized data.
- **Heap:** memory dynamically allocated during execution.
- **Stack:** local variables, function parameters, and return addresses.

A local pointer is on the stack; the memory block it points to after `malloc()` is on the heap. In the usual layout shown, the heap grows upward and the stack downward.

### Process States

As a process executes, it changes state:

- **New:** the process is being created.
- **Ready:** waiting to be assigned to a processor.
- **Running:** instructions are being executed.
- **Waiting/blocked:** waiting for an event, such as I/O completion.
- **Terminated:** execution has finished.

![Pasted image 20261110145806.png](/img/user/Pasted%20image%2020261110145806.png)

State transitions:

- New → Ready: admitted into the system.
- Ready → Running: selected for CPU execution.
- Running → Ready: interrupted or its time slice expires.
- Running → Waiting: must wait for I/O or an event.
- Waiting → Ready: the awaited event has occurred.
- Running → Terminated: process exits.

**Ready** means waiting for the CPU. **Blocked** means waiting for an event or resource.  
→ Event completion moves a process to Ready before it can run again.

**Suspended ready:** a ready process moved from RAM to secondary storage because resources are insufficient.  
**Suspended blocked:** a blocked process moved out of RAM while waiting.

If the event occurs while it is suspended, the process becomes suspended-ready. It still needs to be brought back into memory.

### Life Cycle and Scheduling Queues

Job queue on disk → Job scheduling → Ready queue in RAM → CPU scheduling/dispatching → CPU

- **Job queue:** new jobs waiting on disk to be admitted.
- **Ready queue:** processes in main memory ready and waiting for the CPU.
- **Blocked/device queue:** processes waiting for a resource or I/O.
- **Suspended queue:** processes moved out of main memory.

Job scheduling brings a job into memory. CPU scheduling selects a ready process. Dispatching gives it control of the CPU.

### Process Control Block (PCB)

A **Process Control Block (PCB)** is a data structure maintained by the OS that stores essential information about a process.  
→ Also called Task Control Block.

- Process ID (PID): unique identifier.
- Process state: running, waiting, etc.
- Program counter: location of the next instruction to execute.
- CPU registers: saved processor state.
- CPU scheduling information: priorities and scheduling-queue pointers.
- Memory-management information: memory allocated to the process.
- Accounting information: CPU usage, time limits, and resource information.
- I/O status information: devices allocated to the process and related I/O state.

The **process table** stores process IDs and pointers/references to their PCBs.

![Pasted image 20261110150604.png](/img/user/Pasted%20image%2020261110150604.png)

### Context Switch

A **context switch** occurs when the CPU switches from one process to another. The OS saves the state of the old process and loads the saved state of the new process.

Context-switch time is **overhead**: the CPU does no application work while switching. More state to save and restore can increase the cost.

Multitasking, interrupts, and blocking system calls can lead to a context switch. Entering kernel mode alone does not necessarily switch processes; the same process may continue afterward.

### Schedulers

**Long-term Scheduler (Job Scheduler)**

- Controls which processes are admitted from the job pool on disk into main memory.
- Does not run very frequently because a process spends some time in the system before completing.

**Short-term Scheduler (CPU Scheduler)**

- Selects a process from the ready queue to execute on the CPU.
- Runs frequently; a process may execute for only a few milliseconds before waiting for I/O.

**Medium-term Scheduler (Swapper)**

- Swaps processes from memory to disk, suspending them.
- Later swaps them back in, based on memory pressure and process priority.

### Dispatcher

The **dispatcher** gives the CPU to the process selected by the short-term scheduler.

Its functions:

- Context switching.
- Switching to user mode.
- Jumping to the saved program-counter location.

### Process Creation

Four main events cause process creation:
1. System initialization.
2. A running process executes a process-creation system call.
3. A user requests a new process.
4. A batch job is initiated.

**Foreground processes** interact with users.  
**Background processes** perform specific tasks without direct interaction. Those providing services such as printing, mail, or web serving are called **daemons**.

When creating a process, the OS:
1. Assigns a PID.
2. Creates a PCB.
3. Allocates resources.
4. Loads or maps the program into memory.
5. Initializes the CPU state.
6. Adds the process to the ready queue.

Parent and child may share resources, share a subset, or have independent resources. They can execute concurrently, or the parent can wait for the child.

### fork(), exec(), wait()

**UNIX/Linux:**

- `fork()`: creates a child process. Both parent and child continue after the call.
- `exec()`: replaces the calling process's program image with a new program.
- `wait()`: the parent waits for a child and collects its exit status.

Return value of `fork()`:

- `pid > 0`: parent; the value is the child's PID.
- `pid == 0`: child.
- `pid < 0`: creation failed.

The child often calls `exec()`, but any process can replace its own program. A successful `exec()` does not return to the old program and does not create another process.

![Pasted image 20261110154332.png](/img/user/Pasted%20image%2020261110154332.png)

**Windows:** `CreateProcess()` creates a new process.

### Process Hierarchy

A parent can create several child processes. Children can create their own children, forming a **process tree**.

In Unix, **init (PID 1)** is introduced as the parent of all processes. A process tree and a process group are different concepts.

Windows uses a **handle** to refer to and control a created process. Its process relationships do not follow the same Unix-style model.

### Process Termination

A process may terminate because of:

- Normal completion (`exit`).
- Runtime error, exception, or fatal error.
- Forced termination by another process.
- Parent termination in a system using cascading termination.
- Exceeding a time limit.
- Deadlock or unavailable resources leading the OS to terminate it.

The process calls `exit()` or is killed. The OS releases its active resources, but exit-status information may remain until the parent collects it. The remaining process-table entry can then be removed.

**Cascading termination** means terminating child processes when their parent terminates. Linux does not generally require this.

### Zombie and Orphan Processes

A **zombie process** has completed execution, but its parent has not read its exit status. It no longer runs; a small entry remains in the process table until the parent calls `wait()`.

An **orphan process** is a child whose parent has terminated while the child is still alive. It is adopted by `init` (PID 1), or a designated subreaper on Linux.

- Zombie example: parent sleeps, child exits, parent has not collected the status.
- Orphan example: parent exits, child is still sleeping/running.

![Pasted image 20261110160052.png](/img/user/Pasted%20image%2020261110160052.png)

## IPC

**Interprocess Communication (IPC)** allows processes to communicate with one another.

An **independent process** cannot affect or be affected by another process's execution.  
**Cooperating processes** affect one another and may share data and information.

Reasons for cooperation:

- Sharing data.
- Coordinating activities.
- Managing resources.
- Achieving modularity.

Two fundamental IPC models:

- Shared memory.
- Message passing.

Other mechanisms: pipes, semaphores, signals, sockets, and Remote Procedure Calls (RPCs).

### Shared Memory

IPC using **shared memory** requires communicating processes to establish a shared-memory region. Processes exchange information by reading and writing data in this region.

Other participating processes attach/map the region into their address spaces. After setup, access uses ordinary memory reads and writes.

The processes are responsible for coordinating access so they do not make conflicting changes to the same data.

### Producer-Consumer Problem

A **producer** produces information that is consumed by a **consumer**.  
→ Compiler → Assembler. Web server → Web browser.

A shared buffer lets both processes run concurrently. The producer fills the buffer and the consumer empties it.

**Unbounded buffer:** no practical size limit in the model.

- The consumer waits when no items are available.
- The producer does not wait for free space.

**Bounded buffer:** fixed size.

- The consumer waits when the buffer is empty.
- The producer waits when the buffer is full.

### Bounded-Buffer Solution

```c
#define BUFFER_SIZE 10
item buffer[BUFFER_SIZE];
int in = 0;
int out = 0;
```

`in` points to the next free position.  
`out` points to the next item to consume.

- Empty: `in == out`.
- Full: `(in + 1) % BUFFER_SIZE == out`.
- Maximum number of items: `BUFFER_SIZE - 1`.

One position is left unused to distinguish full from empty. A buffer of size 10 therefore holds 9 items. `% BUFFER_SIZE` wraps the index back to the beginning.

Producer:

```c
while (true) {
    /* Produce next_produced. */
    while ((in + 1) % BUFFER_SIZE == out)
        ;
    buffer[in] = next_produced;
    in = (in + 1) % BUFFER_SIZE;
}
```

Consumer:

```c
while (true) {
    while (in == out)
        ;
    next_consumed = buffer[out];
    out = (out + 1) % BUFFER_SIZE;
    /* Consume next_consumed. */
}
```

The empty loops are **busy waiting**. This shows the buffer logic; a working concurrent implementation also needs correct synchronization.

### Message Passing

**Message passing** allows processes to communicate and synchronize without sharing the same address space. It is useful in distributed systems, where processes may run on different machines.

Basic operations:

- `send(message)`.
- `receive(message)`.

Messages may have fixed or variable size. Communicating processes need a communication link.

The link can use:

- Direct or indirect communication.
- Synchronous or asynchronous communication.
- Automatic or explicit buffering.

### Direct Communication

Processes explicitly identify one another.

**Symmetric:** both sides name the other process.

- `send(P, message)`: send to process P.
- `receive(Q, message)`: receive from process Q.

**Asymmetric:** the sender names the receiver, but the receiver can accept from any sender. The receive operation reports the sender's identity.

### Indirect Communication

Messages are sent to and received from **mailboxes/ports**. Each mailbox has a unique identifier. Processes place messages into it and remove messages from it.

Operations:

- Create a mailbox.
- Send and receive messages through it.
- Destroy the mailbox.

### Blocking and Non-Blocking

Message passing may be blocking or non-blocking.

**Blocking** is synchronous:

- Blocking send: the sender waits until the message is received.
- Blocking receive: the receiver waits until a message is available.

**Non-blocking** is asynchronous:

- Non-blocking send: the sender sends and continues.
- Non-blocking receive: returns an available message or indicates that no message is available.

### Buffering

Messages are held in a temporary queue.

- **Zero capacity:** no queued messages; sender waits for receiver.
- **Bounded capacity:** finite queue; sender waits when it is full.
- **Unbounded capacity:** unlimited queue in the model; sender does not wait for buffer space.

### Shared Memory and Message Passing

**Message passing** is useful for smaller exchanges and is easier to implement across networked computers. It commonly requires system calls and kernel intervention.

**Shared memory** can be faster because accesses are ordinary memory operations after setup. The processes must synchronize access to the shared data.

### Pipes

A **pipe** is an IPC mechanism that carries data between processes.

Things to consider:

- One-way or two-way communication?
- Half duplex or full duplex?
- Must the processes have a parent-child relationship?
- Local communication or communication over a network?

**Half duplex:** data travels in one direction at a time.  
**Full duplex:** data travels in both directions simultaneously.

**Ordinary/anonymous pipes** are commonly used between parent and child processes. In Unix, they are one-way: the producer writes to one end and the consumer reads from the other.
→ Two-way communication requires two pipes.

**On Unix systems:**

- `pipe(fd)`: creates a pipe.
- `fd[0]`: read end.
- `fd[1]`: write end.
- `read()` and `write()`: transfer data.
- `close()`: closes an end of the pipe.

**On Windows systems:**

- `CreatePipe()`: creates an anonymous pipe.
- `ReadFile()`: reads from the pipe.
- `WriteFile()`: writes to the pipe.

### Named Pipes

**Named pipes** do not require a parent-child relationship. Several processes can use an established named pipe.

**Unix:** named pipes are called **FIFOs**. They are local and normally used as one-way byte streams.

- `mkfifo()`: creates the FIFO.
- `open()`, `read()`, `write()`, `close()`: access it.

**Windows:** named pipes can support full-duplex and network communication.

- `CreateNamedPipe()`: creates the pipe.
- `ConnectNamedPipe()`: the server waits for a client connection.
- `ReadFile()` and `WriteFile()`: transfer data.

### Sockets

A **socket** is an endpoint for communication. A pair of processes communicating over a network uses a pair of sockets, one for each process.

A network socket endpoint is identified by an **IP address and port number**.

![Pasted image 20261111122956.png](/img/user/Pasted%20image%2020261111122956.png)

### Remote Procedure Calls (RPCs)

**RPC** allows a local machine (client) to call a procedure on a different machine (server).

The call is written similarly to a local procedure call, while the RPC mechanism handles the remote interaction.

Client function → Client stub/runtime → Request → Server runtime/stub → Server function → Reply

The client resumes with the result after receiving the reply.

![Pasted image 20261111131540.png](/img/user/Pasted%20image%2020261111131540.png)

## Koll1

Questions shown in Koll1:

- Interrupts and traps; keyboard input; user mode and kernel mode.
- Benefit of multitasking.
- Clustered/distributed systems, client-server, P2P, cloud, and virtualization.
- Explain three OS services.
- Draw how a process invokes a system call.
- Explain modular structure and its disadvantages.
- Draw the path from the job queue on disk to the CPU.
- Explain the three schedulers.
- Match events to process-state transitions.
- Count processes and printed lines with `fork()`.
- Recognize zombie and orphan examples.

For `fork()` counting, follow where the print statement is placed:

- Two successful unconditional forks executed by every process give **4 processes total**, including the original: **3 new child processes**.
- Print after each fork in a two-iteration loop: `2 + 4 = 6` prints.
- Print before each fork: `1 + 2 = 3` prints.
- Print after the loop: `4` prints.

These counts assume successful forks and that earlier output has been flushed before forking.

True/false points:

- Keyboard input generates a hardware interrupt.
- Saving context during an interrupt does not always mean switching to another process.
- Clusters can support load balancing.
- Distributed computers do not all share one physical memory.
- Client-server systems are suitable for internet applications.
- P2P peers can act as both client and server.
- Cloud computing delivers computing resources over the internet.
- Virtualization is not limited to Windows.
