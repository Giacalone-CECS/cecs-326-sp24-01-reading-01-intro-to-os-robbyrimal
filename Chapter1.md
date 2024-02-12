# Reading 1 - Introduction to OS  

1. What are the two main functions of an operating system?

   1. Providing abstractions to user programs -> Execute and provide services for application software

   2. Managing the computer's resources -> CPU, Memory, I/O

2. What is the difference between timesharing and multiprogramming systems?

    1. **Multiprogramming** allowed for executing multiple programs at the same time to now keep the CPU busy 100% of the time instead of just sitting Idle while it waits for I/O to finish.

    2. **Timesharing** is a *variant* of multiprogramming, where multiple users has an online terminal and wanted to use it at the same time. Whenever the CPU would be idle, it would handle other user jobs that want service.

3. The family-of-computers idea was introduced in the 1960s with the IBM System/360 mainframes. Is this idea now dead as a doornail does it live on?

   * The **family-of-computers** idea still lives on today as group of different configurations of computer systems in performance and pricing can still run the same software on the same OS.

4. What is the difference between kernel and user mode? Explain how having two distinct modes aids in designing an operating system.

    1. The most fundamental piece of software runs on **kernel mode** (supervisor mode). It has complete access to all of the hardware and can execute any instruction the machine is capable of executing.  

    2. The rest of the software runs on **user mode** which is only a subset of machine instructions available and applications at user level cannot modify or have direct access to system resources.  

    * **Having two distinct modes allows the system to better utilize resources effectively, as user mode gets limited resources compared to the kernel.**

5. On early computers, every byte of data read or written was handled by the CPU (i.e., there was no DMA). What implications does this have for multiprogramming?  

    * Without a Direct Memory Access (DMA) chip that can control the flows of bits between memory, the CPU would be fully occupied with handling I/O jobs.

    * **The reason multiprogramming exists in the first place, is to give the CPU something to do while waiting for I/O to complete.**

6. There are several design goals in building an operating system, for example, resource utilization, timeliness, robustness, and so on. Give an example of two design goals that may contradict one another.

    1. **Stability** - Having a fully vetted, robust operating system would ensure one that is stable and pleasant to use.  

    2. **Flexible** - Having a general purpose operating system that could be used on any device.

    **These two goals can contradict with one another because optimizations made in consideration to the devices hardware could impact the flexibility to be run on all devices, and making a operating system with flexibility in mind could be detrimental to the stability and robustness across different devices.**

7. Which of the following instructions should be allowed only in kernel mode?
    * [x] Disable all interrupts.  
    * [ ] Read the time-of-day clock.  
    * [ ] Set the time-of-day clock.
    * [ ] Change the memory map.  

8. Consider a system that has two CPUs, each CPU having two threads (hyper-threading). Suppose three programs, P0, P1, and P2, are started with run times of 5, 10 and 20 msec, respectively. How long will it take to complete the execution of these programs? Assume that all three programs are 100% CPU bound, do not block during execution, and do not change CPUs once assigned.  

    <center>

    | CPU and Threads     | Execution Time | Program |
    |:-------------------:|:-------------:|:--------:|
    | Core 1, Thread 1     | 5 ms          |   P0    |
    | Core 1, Thread 2     | 10 ms         |   P1    |
    | Core 2, Thread 1     | 20 ms         |   P2    |
    | **Total Time**       | **20 ms**     |         |

    </center>
   1. Since the programs execute concurrently, it will take 20 ms to complete the execution of these programs.

9. What is a trap instruction? Explain its use in operating systems.

    1. A trap instruction allows switching between user and kernel modes.

    2. If a user program requires elevated privileged and needs to make a system call, it will execute a trap instruction.  

10. Modern operating systems decouple a process address space from the machine’s physical memory. List two advantages of this design.

    1. The operating system keeps part of the address space in main memory and park on disk, swapping as needed. It will create an abstraction of an address as the set of addresses a process may reference.  

    2. Processes can continue execution without waiting for additional space in main memory, improving overall system efficiency.
