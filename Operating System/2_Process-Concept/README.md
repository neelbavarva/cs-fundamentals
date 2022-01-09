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

## Different Types of 

Processes are two types based on their types of categories. The first one which you mentioned is related to event-specific process categorization and the next categorization is based on their nature.

<strong>1. Event-specific </strong>Event-specific based category of process

- CPU Bound Process: Processes that spend the majority of their time simply using the CPU (doing calculations).
- I/O Bound Process: Processes that are associated with input/output-based activity like reading from files, etc.

<strong>2.</strong> Category of processes based on their <strong>nature</strong>

- Independent Process: A process that does not need any other external factor to get triggered is an independent process.
- Cooperative Process: A process that works on the occurrence of any event and the outcome affects any part of the rest of the system is a cooperating process.

But, Threads have got only one classification based on their nature(Single Level Thread and Multi-Level Threads).

Actually, in modern operating systems, there are two levels at which threads operate. They are system or kernel threads and user-level threads. This one is generally not the classification, though some of them freely do classify. It is a misuse.


