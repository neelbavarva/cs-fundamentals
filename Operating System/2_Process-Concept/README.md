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
