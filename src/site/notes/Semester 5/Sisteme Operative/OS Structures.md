---
{"dg-publish":true,"permalink":"/semester-5/sisteme-operative/os-structures/","dg-note-properties":{}}
---

Various popular implementations of OS structures: 
- Simple structure 
- Monolithic structure 
- Layered structure 
- Microkernel structure 
- Modular structure
- Hybrid-kernel structure

# Simple Structure

It is the simplest OS Structure and is not well defined; It can only be used for small and limited systems.
Has no distinction between user and kernel modes, allowing all programs direct access to the underlying hardware. → MS-DOS is an example of such OS.

![Pasted image 20261113222407.png](/img/user/Pasted%20image%2020261113222407.png)

**Advantages:** 
✓ Easy to develop. 
✓ Good performance. 
✓ Minimal overhead. 

**Disadvantages:**
x If one user program fails, the entire OS crashes. 
x Limited functionality. 
x It does not enforce data hiding in the OS

# Monolithic Structure

Monolithic Structure is an OS architecture in which most OS services run together within a single large kernel in kernel mode. 
The kernel acts as a manager by managing all things like file management, memory management, devices management, and operational processes. 
Kernel delivers basic services to all other elements of the system.
![Pasted image 20261113222542.png](/img/user/Pasted%20image%2020261113222542.png)

**Advantages:**
✓ Simple design and implementation. 
✓ It is easier to build because all parts are in one code block. 
✓ Performance is fast since everything runs in a single block, therefore communication between components is swift. 

**Disadvantages:**
x If any service in the monolithic kernel fails, the entire system fails. 
x Difficult to extend or modify, as any changes to one component may require changes to other parts of the OS. 
x This structure can lead to issues such as a larger kernel size, which can impact system performance and stability.

# Layered Structure

OS is divided into layers or levels. 
The hardware is on the bottom layer (layer 0), while the user interface is on the top layer (layer N).  
These layers are arranged in a hierarchical way in which the top-level layers use the functionalities of their lower-level levels.
![Pasted image 20261113222829.png](/img/user/Pasted%20image%2020261113222829.png)

**Advantages:**
✓ This approach helps to modularize the OS, making it easier to understand, maintain, and extend. 
✓ Functionalities of each layer are isolated, and abstraction is also available. 
✓ Simplicity of construction and debugging. 

**Disadvantages:**
x Performance overhead associated with the communication between layers. 
x It takes careful planning to construct the layers since higher layers only utilize the functions of lower layers.

# Microkernel Structure

This structure designs the OS by removing all non-essential components - only essential functions run in the kernel; other services run in user space. → This results in a smaller kernel called the microkernel.
Communication takes place between user modules using message passing.
![Pasted image 20261113223531.png](/img/user/Pasted%20image%2020261113223531.png)

**Advantages:**
✓ If any component or microkernel fails, the remaining OS is unaffected and continues to function normally. 
✓ Easier to extend a microkernel.
✓ It allows the OS to be portable between platforms. 
✓ More reliable (less code is running in kernel mode). 
✓ Enhanced system stability and security. 

**Disadvantages:** 
x Performance overhead of user space to kernel space communication. 
x System is complex to be constructed. 
x Complexity in managing user-space components.

# Modular Structure

The OS is divided into a set of independent modules. 
Each module is responsible for a specific task, such as memory management, process scheduling, or device drivers. 
Modules can be loaded and unloaded dynamically, as needed. → OSes implement Loadable Kernel Modules (LKMs).
LKMs can be “inserted” into the kernel as the system is started (or booted) or during run time, such as when a USB device is plugged into a running machine.

![Pasted image 20261113223908.png](/img/user/Pasted%20image%2020261113223908.png)

**Advantages:**
✓ High modularity, it easier to understand, develop, and maintain the OS. 
✓ Very flexible. New modules can be added easily, and existing modules can be modified or removed without affecting the rest of the OS. 

**Disadvantages:**
x Performance overhead associated with the communication between modules. 
x More complex, because the modules must be carefully designed to ensure that they interact correctly.

# Hybrid-kernel Structure

A hybrid-kernel structure combines elements of both monolithic and microkernel structures to balance performance, flexibility, and reliability. 
The core of the hybrid-kernel is a small microkernel that provides essential services.

**Advantages:** 
✓ Good performance because frequently used services can be implemented as modules in user space, which avoids the overhead of system calls.
✓ It supports a wide range of hardware and applications. 
✓ It provides better isolation and security by implementing microkernel approach. 

**Disadvantages:** 
x It increases overall complexity of system by implementing both structure (monolithic and microkernel). 
x Performance overhead associated with IPC between the microkernel and the modules in user space.

## Most modern OSes are actually not one pure model.

- For example, Linux is monolithic, because having the OS in a single address space provides very efficient performance. However, it also modular, so that new functionality can be dynamically added to the kernel. 
- Windows is largely monolithic, but it retains some behavior typical of microkernel systems, including providing support for separate subsystems that run as user-mode processes. Windows systems also provide support for dynamically loadable kernel modules (LKMs).