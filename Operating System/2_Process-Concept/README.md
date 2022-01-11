## Program and Process

<strong>Program : </strong>When we execute a program that was just compiled, the OS will generate a process to execute the program. Execution of the program starts via GUI mouse clicks, command line entry of its name, etc. A program is a passive entity as it resides in the secondary memory, such as the contents of a file stored on disk. One program can have several processes. 

<strong>Process : </strong>The term process (Job) refers to program code that has been loaded into a computer’s memory so that it can be executed by the central processing unit (CPU). A process can be described as an instance of a program running on a computer or as an entity that can be assigned to and executed on a processor. A program becomes a process when loaded into memory and thus is an active entity. 

## States of a Process in Operating Systems

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20190604122001/states_modified.png" />

- <strong>New(Create)</strong> In this step, the process is about to be created but not yet created, it is the program which is present in secondary memory that will be picked up by OS to create the process.
- <strong>Ready</strong> New -> Ready to run. After the creation of a process, the process enters the ready state i.e. the process is loaded into the main memory. The process here is ready to run and is waiting to get the CPU time for its execution. Processes that are ready for execution by the CPU are maintained in a queue for ready processes.
- <strong>Run</strong> The process is chosen by CPU for execution and the instructions within the process are executed by any one of the available CPU cores.
- <strong>Blocked or Wait</strong> Whenever the process requests access to I/O or needs input from the user or needs access to a critical region(the lock for which is already acquired) it enters the blocked or wait state. The process continues to wait in the main memory and does not require CPU. Once the I/O operation is completed the process goes to the ready state.
- <strong>Terminated or Completed</strong> Process is killed as well as PCB is deleted.
- <strong>Suspend Ready</strong> Process that was initially in the ready state but were swapped out of main memory(refer Virtual Memory topic) and placed onto external storage by scheduler are said to be in suspend ready state. The process will transition back to ready state whenever the process is again brought onto the main memory.
- <strong>Suspend Wait or Suspend Block</strong> Similar to suspend ready but uses the process which was performing I/O operation and lack of main memory caused them to move to secondary memory. When work is finished it may go to suspend ready.

## Different Types of Process

Processes are two types based on their types of categories. The first one which you mentioned is related to event-specific process categorization and the next categorization is based on their nature.

<strong>1. Event-specific </strong>Event-specific based category of process

- CPU Bound Process: Processes that spend the majority of their time simply using the CPU (doing calculations).
- I/O Bound Process: Processes that are associated with input/output-based activity like reading from files, etc.

<strong>2.</strong> Category of processes based on their <strong>nature</strong>

- Independent Process: A process that does not need any other external factor to get triggered is an independent process.
- Cooperative Process: A process that works on the occurrence of any event and the outcome affects any part of the rest of the system is a cooperating process.

But, Threads have got only one classification based on their nature(Single Level Thread and Multi-Level Threads).

Actually, in modern operating systems, there are two levels at which threads operate. They are system or kernel threads and user-level threads. This one is generally not the classification, though some of them freely do classify. It is a misuse.

## Process Table and Process Control Block (PCB)

While creating a process the operating system performs several operations. To identify the processes, it assigns a process identification number (PID) to each process. As the operating system supports multi-programming, it needs to keep track of all the processes. For this task, the process control block (PCB) is used to track the process’s execution status. Each block of memory contains information about the process state, program counter, stack pointer, status of opened files, scheduling algorithms, etc. All these information is required and must be saved when the process is switched from one state to another. When the process makes a transition from one state to another, the operating system must update information in the process’s PCB.

A process control block (PCB) contains information about the process, i.e. registers, quantum, priority, etc. The process table is an array of PCB’s, that means logically contains a PCB for all of the current processes in the system.

<img width=200 src="https://media.geeksforgeeks.org/wp-content/uploads/process-table.jpg" />

- <strong>Pointer</strong> - It is a stack pointer which is required to be saved when the process is switched from one state to another to retain the current position of the process.
- <strong>Process State</strong> - It stores the respective state of the process.
- <strong>Process Number</strong> - Every process is assigned with a unique id known as process ID or PID which stores the process identifier.
- <strong>Program Counter</strong> - It stores the counter which contains the address of the next instruction that is to be executed for the process.
- <strong>Register</strong> - These are the CPU registers which includes: accumulator, base, registers and general purpose registers.
- <strong>Memory Limits</strong> - This field contains the information about memory management system used by operating system. This may include the page tables, segment tables etc.
- <strong>Open Files List</strong> - This information includes the list of files opened for a process.

## How does a process look like in memory?

A program loaded into memory and executing is called a process. In simple, a process is a program in execution.

When a program is created then it is just some pieces of Bytes which is stored in Hard Disk as a passive entity. Then the program starts loading in memory and become an active entity, when a program is double-clicked in windows or entering the name of the executable file on the command line. (i.e. a.out or prog.exe)

Let’s look at each memory segment and how does a process look like within memory −

<img src="https://www.tutorialspoint.com/assets/questions/media/29467/1.jpg" />

<strong>Text</strong> : A process is more than the program code or a code segment is known as Text Section. This section of memory contains the executable instructions of a program. It also contains constants, macros and it is read-only segment to prevent accidentally modification of an instruction. It is also sharable so that the so that another process can use this whenever it is required.

<strong>Data</strong> : Next Data Section segment of memory contains the global and static variables that are initialized by the programmer prior to the execution of a program. This segment is not read-only, as the value of the variables can be changed at the runtime.

```
#include<stdio.h>
int b;//will be stored in data section
int main(){
   static int a; //will be stored in data section
   return;
}
```

<strong>Heap</strong> : To allocate memory for variables whose size cannot be statically determined by the compiler before program execution, requested by the programmer, there is a requirement of dynamic allocation of memory which is done in heap segment. It can be only determined at run-time. It is managed via system calls to malloc, calloc, free, delete etc. An C example: malloc(2) return the starting address of the 2 BYTE block which is in heap area.

<strong>Stack</strong> : A process generally also includes the process stack, which contains temporary data i.e. function parameters, return addresses, and local variables. On the standard x86 architecture it grows downwards to lower addresses but on some other architectures it may grow the opposite direction.it is shown in the diagram that stack grows opposite direction of heap for avoiding overlapping problem. This section is committed to store all the data needed by a function call in a program.

A stack pointer register keeps the tracks of the top of the stack i.e., how much of the stack area using by the current process, and it is modified each time a value is “pushed” onto the stack. If the stack pointer meets the heap pointer the available free memory is depleted.

## Process and Thread

<strong>Process</strong> : Process are basically the programs which are dispatched from the ready state and are scheduled in the CPU for execution. PCB(Process Control Block) holds the concept of process. A process can create other processes which are known as Child Processes. The process takes more time to terminate and it is isolated means it does not share the memory with any other process. 

The process can have the following states like new, ready, running, waiting, terminated, suspended. 

<strong>Thread</strong> : Thread is the segment of a process means a process can have multiple threads and these multiple threads are contained within a process. A thread has three states: Running, Ready, and Blocked. 

Thread takes less time to terminate as compared to process but unlike process threads do not isolate. 

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20190522155604/Untitled-Diagram-361.png" />

## Process Scheduling

The process scheduling is the activity of the process manager that handles the removal of the running process from the CPU and the selection of another process on the basis of a particular strategy.

Process scheduling is an essential part of a Multiprogramming operating systems. Such operating systems allow more than one process to be loaded into the executable memory at a time and the loaded process shares the CPU using time multiplexing.

<hr>

### Process Scheduling Queues

The OS maintains all PCBs in Process Scheduling Queues. The OS maintains a separate queue for each of the process states and PCBs of all processes in the same execution state are placed in the same queue. When the state of a process is changed, its PCB is unlinked from its current queue and moved to its new state queue.

The Operating System maintains the following important process scheduling queues −

- <strong>Job Queue</strong> : This queue keeps all the processes in the system.
- <strong>Ready Queue</strong> : This queue keeps a set of all processes residing in main memory, ready and waiting to execute. A new process is always put in this queue.
- <strong>Device Queues</strong> : The processes which are blocked due to unavailability of an I/O device constitute this queue.

<img src="https://www.tutorialspoint.com/operating_system/images/queuing_diagram.jpg" />

The OS can use different policies to manage each queue (FIFO, Round Robin, Priority, etc.). The OS scheduler determines how to move processes between the ready and run queues which can only have one entry per processor core on the system; in the above diagram, it has been merged with the CPU.

### Schedulers

Schedulers are special system software which handle process scheduling in various ways. Their main task is to select the jobs to be submitted into the system and to decide which process to run. Schedulers are of three types −

- Long-Term Scheduler
- Short-Term Scheduler
- Medium-Term Scheduler

<strong>Long-Term Schedular</strong> : It is also called a job scheduler. A long-term scheduler determines which programs are admitted to the system for processing. It selects processes from the queue and loads them into memory for execution. Process loads into the memory for CPU scheduling.

The primary objective of the job scheduler is to provide a balanced mix of jobs, such as I/O bound and processor bound. It also controls the degree of multiprogramming. If the degree of multiprogramming is stable, then the average rate of process creation must be equal to the average departure rate of processes leaving the system.

On some systems, the long-term scheduler may not be available or minimal. Time-sharing operating systems have no long term scheduler. When a process changes the state from new to ready, then there is use of long-term scheduler.

<strong>Short-Term Schedular</strong> : It is also called as CPU scheduler. Its main objective is to increase system performance in accordance with the chosen set of criteria. It is the change of ready state to running state of the process. CPU scheduler selects a process among the processes that are ready to execute and allocates CPU to one of them.

Short-term schedulers, also known as dispatchers, make the decision of which process to execute next. Short-term schedulers are faster than long-term schedulers.

<strong>Medium Term Schedular</strong> : Medium-term scheduling is a part of swapping. It removes the processes from the memory. It reduces the degree of multiprogramming. The medium-term scheduler is in-charge of handling the swapped out-processes.

A running process may become suspended if it makes an I/O request. A suspended processes cannot make any progress towards completion. In this condition, to remove the process from memory and make space for other processes, the suspended process is moved to the secondary storage. This process is called swapping, and the process is said to be swapped out or rolled out. Swapping may be necessary to improve the process mix.

![image](https://user-images.githubusercontent.com/62550592/148726498-a407cd9d-ca5a-45f0-a18d-34283c70fbca.png)

<hr>

## CPU bound and I/O bound

<strong>CPU Bound</strong> means the rate at which process progresses is limited by the speed of the CPU. A task that performs calculations on a small set of numbers, for example multiplying small matrices, is likely to be CPU bound.

<strong>I/O Bound</strong> means the rate at which a process progresses is limited by the speed of the I/O subsystem. A task that processes data from disk, for example, counting the number of lines in a file is likely to be I/O bound.

<strong>Memory bound</strong> means the rate at which a process progresses is limited by the amount memory available and the speed of that memory access. A task that processes large amounts of in memory data, for example multiplying large matrices, is likely to be Memory Bound.

<strong>Cache bound</strong> means the rate at which a process progress is limited by the amount and speed of the cache available. A task that simply processes more data than fits in the cache will be cache bound.

I/O Bound would be slower than Memory Bound would be slower than Cache Bound would be slower than CPU Bound.

## Context Switching

Context Switching involves storing the context or state of a process so that it can be reloaded when required and execution can be resumed from the same point as earlier. This is a feature of a multitasking operating system and allows a single CPU to be shared by multiple processes.

<img src="https://www.tutorialspoint.com/operating_system/images/context_switch.jpg" />

<hr> 

### Context Switching Triggers

- <strong>Multitasking</strong> : In a multitasking environment, a process is switched out of the CPU so another process can be run. The state of the old process is saved and the state of the new process is loaded. On a pre-emptive system, processes may be switched out by the scheduler.

- <strong>Interrupt Handling</strong> : The hardware switches a part of the context when an interrupt occurs. This happens automatically. Only some of the context is changed to minimize the time required to handle the interrupt.

- <strong>User and Kernel Mode Switching</strong> : A context switch may take place when a transition between the user mode and kernel mode is required in the operating system.

 
