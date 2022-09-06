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