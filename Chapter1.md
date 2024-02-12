# Reading 1 - Introduction to OS  

---

1. What are the two main functions of an operating system?

   The two main functions of an operating system are providing abstractions to user programs and managing the computer's resources.  

2. What is the difference between timesharing and multiprogramming systems?

    **Multiprogramming** allowed for executing multiple programs at the same time to now keep the CPU busy 100% of the time instead of just sitting Idle.

    **Timesharing** is a *variant* of multiprogramming, where multitple users has an online terminal and wanted to use it at the same time. Whenever the CPU would be idle, it would handle other user jobs that want service.

3. The family-of-computers idea was introduced in the 1960s with the IBM System/360 mainframes. Is this idea now dead as a doornail does it live on?

   The **family-of-computers** idea still lives on today as group of different configurations of computer systems in performance and pricings can still run the same software on the same OS.

4. What is the difference between kernel and user mode? Explain how having two distinct modes aids in designing an operating system.

    Most computers have two modes of operation: kernel mode and user mode. The most **fundamental** piece of software runs on kernel mode (supervisor mode). It has complete access to the

5. On early computers, every byte of data read or written was handled by the CPU (i.e., there was no DMA). What implications does this have for multiprogramming?

6. There are several design goals in building an operating system, for example, resource utilization, timeliness, robustness, and so on. Give an example of two design goals that may contradict one another.

7. Which of the following instructions should be allowed only in kernel mode?
    - [x] Disable all interrupts.  
    - [ ] Read the time-of-day clock.  
    - [ ] Set the time-of-day clock.
    - [ ] Change the memory map.  

8. Consider a system that has two CPUs, each CPU having two threads (hyperthreading). Suppose three programs, P0, P1, and P2, are started with run times of 5, 10 and 20 msec, respectively. How long will it take to complete the execution of these programs? Assume that all three programs are 100% CPU bound, do not block during execution, and do not change CPUs once assigned.

9. What is a trap instruction? Explain its use in operating systems.

10. Modern operating systems decouple a process address space from the machine’s physical memory. List two advantages of this design.
