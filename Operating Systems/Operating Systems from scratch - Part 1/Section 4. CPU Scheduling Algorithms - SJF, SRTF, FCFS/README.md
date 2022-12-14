# Section 4. CPU Scheduling Algorithms - SJF, SRTF, FCFS

### 12. Types of scheduler, Context switching

Keyword : Long Term Scheduler, Short Term Scheduler, Middle Term Scheduler, Context Switching, 

- Short Term Scheduler(often called as 'Scheduler')
  - It is part of our OS code.
  - It decides which process should get the CPU first(RAM -> CPU).

- Long Term Scheduler
  - It is part of our OS code.
  - It decides which processes should be moved into the RAM(hard disk -> RAM).

- Middle Term Scheduler
  - It is a function or module which is present in OS code.
  - It decides which process should be swapped out of the RAM and high priority process can be swapped into the RAM.  

☆ Every process will have something called as priority. Priority (which is one of the process attributes) is the number which is given to every process. <br>
☆ Every process will have a process control block. <br>
☆ Higher priority process should always be executed first before Lower priority processes. <br>

***
#### [Process Table and Process Control Block (PCB)](https://www.geeksforgeeks.org/process-table-and-process-control-block-pcb/) : PCB에 대한 내용 까먹어서 구글링해봄

While creating a process the operating system performs several operations. **To identify the processes, it assigns a process identification number(PID) to each process.** (중략)... All these information(= attributes of process) is required and must be saved when the process is switched from one state to another. **When the process makes a transition from one state to another, the operating system must update information in the process's PCB.**

☆ The **degree of multiprogramming** describes the maximum number of processes that a single-processor system can accommodate efficiently.

A process control block (PCB) contains information about the process.

<img src="./images/process-table.jpg" height = 30% width = 30%>

- Pointer : It is a stack pointer which is required to be saved when the process is switched from one state to another to retain(유지하다) the current position of the process.
- Process state : It stores the respective(각각의) state of the process.
- Process number : PID which is process identifier.
- Program counter : It stores the counter which contains the address of the next instruction that is to be executed for the process.
- Register : These are the CPU registers which includes : accumulator, base, registers and general purpose registers -> 컴퓨터 구조를 알아야 이해 가능
- 이해가 안 가므로 나머지는 생략...
***
#### [Difference between Swapping and Context Switching](https://www.geeksforgeeks.org/difference-between-swapping-and-context-switching/#:~:text=An%20operating%20system%20uses%20this,between%20one%20process%20and%20another.) : 강의에서 다루지만, 내용이 부실한 것같아 새로 찾아봄

**Programs** are **sets of instructions** designed **to accomplish specific tasks**. Similarly, **a process** refers to **a runtime instance of a computer program**.

1. **Context switching**
An operating system uses this technique to switch a process between states to execute its functions through CPUs. It is a process of **saving the context(state) of the old process(suspend)** and **loading it into the new process(resume)**. It occurs whenever the CPU switches between one process and another. 

2. **Swapping**
This is the process by which a process is temporarily swapped (moved) from the main memory (RAM) to the secondary memory (Disk). The main memory is fast but has less space than secondary storage, so the inactive processes are moved to secondary memory, and the system swaps the memory from secondary to the main memory later. (중략)... Swapping has been divided into two more concepts: Swap-in and Swap-out.

- **Swap-in** is the process of removing a program from a hard disk and moving it back to the main memory or RAM.
- **Swap-out** removes a program from RAM or main memory and moves or stores it to the hard disk or secondary storage.
***

### 13. Various times of a process

Let's see what's the difference between **point in time** and **duration in time**.
- **point in time** vs **duration in time**
  - point in time : 그 때 그 시점의 시간
  - duration in time : 그 떄 그 시점의 시간부터 그 이후의 시점까지의 시간

<br>

- **Various times of a process**
  - **Arrival time** : Point in time. The process is moved from Hard disk to RAM. A program has arrived from hard disk into RAM. That is what we mean by Arrival time.
  - **Completion time** : Point in time. the process has completed its execution, and this process can be removed completely from the RAM.
  - **Turn Around Time (TAT)** : Duration in time. TAT = Completion time - Arrival time, TAT = Burst time + I/O time + Waiting Time
  - **Waiting Time** : Duration in time. Subset of TAT. Waiting time is nothing but, The time spent by a process in the RAM without actually executing. As well as not performing I/O. It is simply waiting inside the RAM to be picked by the CPU, for execution in the future.
  - **Response time** : 나중에 공부함
  - **I/O time** : Duration in time. The amount of time which is spent my a process, which is performing I/O after it has arrived to the RAM, until its completion is called as I/O time. 