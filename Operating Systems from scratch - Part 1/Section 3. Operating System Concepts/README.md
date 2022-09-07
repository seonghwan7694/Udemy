### 7. Program vs Process, States of a process
- Program
  - Executable files which are present in our hard disk.
  - nothing but software
- Process
  - If I clicked the Google Chrome software(= program), a new copy of this program will be created in the hard disk itselft. A new copy of this program is called process.
  - **A single program, multiple processes can be created.**

**State of Process** : Process undergoes various stages.
- New state : Program has actually created process. process is being newly created by program.
- Ready state  : Waiting for some event to happen, which means that process is actually ready for execution(CPU) or for performing I/O. 
- Running state : Process is being executed by the CPU taking line-by-line. Process is being run by CPU or being executed by the CPU. ※ Running == Executing
- I/O state : Process in RAM is performing some I/O event. Process is undergoing I/O. It is also called Block state. ※ Either reading or writing form I/O devices is what we say as I/O
- Terminated state : A process has actally completed its execution, which means it is completely done with everthing. It will be completly removed from the RAM.  
- Suspend Ready state : Explaining later
- Suspend wait state : Explaining later

**Entire journey of program**
   1. Initially it started as a source program then it has been converted into machine code.
   2. Now machine code has been placed inside the hard disk.
   3. And then it has been moved into the RAM.
   4. Now once it has moved into the Ram, it can undergo either I/O or it can be executed by the CPU or it can simply remain in the RAM, waiting for some event to happen (or for execution by CPU ir wauting for I/O)

### 8. Degree of Multiprogramming
Degree of programming is nothing but maximum number of processes which can be present in the RAM of our computer.

For example, I have a computer which has 4GB RAM. Assume that a size of a single process is 4KB. Now, My computer can have $2^{20}$ processes inside the RAM.

** 참고 : 1KB = $2^{10}$, 1MB = $2^{20}$, 1GB = $2^{30}$, 1TB = $2^{40}$, 1Byte = 8 bits

### 9. Types of Operating Systems

☆ **CPU efficiency** = **Useful time of CPU**(CPU가 실제로 일한 시간) / **Total Time of CPU**(컴퓨터 켠 후 지금까지의 시간)

FASTNESS : Batch OS < Multiprogramming OS < Multiprocessing OS

1. **Batch operating system** : degree of multiprogramming is always 1. That means, only one process can be placed inside the RAM.
CPU(execution) and I/O devices can work in parrallel. But, Execution and I/O devices can't be done at the same time for 'a particular process'. Parrallel means that if a process is being executed by CPU, I/O is working for another process vice versa.
So, Batch operating system is the most lowest 'CPU efficiency' compare to other OS. Because a process is done by CPU or I/O devices, then taking a another process from hard disk to RAM. If a another process needs I/O devices, CPU is doing nothing. Less CPU efficiency means computer is slow.

<br>

2. **Multiprogramming operating system** : degree of multiprogramming is more than 1. That means, We can have more than one process in the RAM. It makes CPU efficiency improve. Which means if one of the processes is undergoing I/O, at the same time I can execute some other process. Which menas, I'm not allowing the CPU to remain idle. So CPU efficiency is going to improve in multiprogramming ooperating systems.

<br>

3. **Multiprocessing operating system** : This OS can have more than one CPU. Whatever we are using today in our computers is multi-processing operating systems. (Octa core processor, Quad core processor means that in my computer there are 6, 8 processor each.) This means one process is being executed by this CPU(central processing unit), some other process will also be executed by this another CPU.

☆ **Parallel processing(병렬 연산)** vs **Concurrent processing(동시 연산)** - 전체적으로 이해를 못하겠음.
Parrallel processing means, we are executing more than one process at the same time. Multiprocessing OS is actually doing concurrent processing.
Definitely parallel processing will be faster than concurrent processing. But actually the disadvantage with that si in parrallel processing the system cost will increase.

☆ Batch OS and Multiprogramming OS can have only one CPU. But multiprocessing OS can have more than one CPU. 