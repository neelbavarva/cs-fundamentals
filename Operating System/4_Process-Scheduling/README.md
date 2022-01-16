## Process Scheduling

Process Scheduling is an OS task that schedules processes of different states like ready, waiting, and running. Process scheduling allows OS to allocate a time interval of CPU execution for each process. Another important reason for using a process scheduling system is that it keeps the CPU busy all the time. This allows you to get the minimum response time for programs.

## CPU Burst and I/O Burst

Burst is the amount of time required by a process or can be said the amount of time required by the process to finish.

A CPU bursts when it is executing instructions; an I/O system bursts when it services requests to fetch information. The idea is that each component operates until it can’t.

A CPU can run instructions from cache until it needs to fetch more instructions or data from memory. That ends the CPU burst and starts the I/O burst. The I/O burst read or writes data until the requested data is read/written or the space to store it cache runs out. That ends an I/O burst.

## CPU Scheduling

CPU Scheduling is a process of determining which process will own CPU for execution while another process is on hold. The main task of CPU scheduling is to make sure that whenever the CPU remains idle, the OS at least select one of the processes available in the ready queue for execution.

![image](https://user-images.githubusercontent.com/62550592/149648442-3ac70ff2-7091-432e-b2d6-b145e7b20b8b.png)

<hr>

### Types of CPU Scheduling

- <strong>Preemptive Scheduling</strong> : In Preemptive Scheduling, the tasks are mostly assigned with their priorities. Sometimes it is important to run a task with a higher priority before another lower priority task, even if the lower priority task is still running. The lower priority task holds for some time and resumes when the higher priority task finishes its execution.
- <strong>Non-Preemptive Scheduling</strong> : In this type of scheduling method, the CPU has been allocated to a specific process. The process that keeps the CPU busy will release the CPU either by switching context or terminating. It is the only method that can be used for various hardware platforms. That’s because it doesn’t need special hardware (for example, a timer) like preemptive scheduling.

To determine if scheduling is preemptive or non-preemptive, consider these four parameters:
1. A process switches from the running to the waiting state.
2. Specific process switches from the running state to the ready state.
3. Specific process switches from the waiting state to the ready state.
4. Process finished its execution and terminated.

_Only conditions <strong>1 and 4</strong> apply, the scheduling is called <strong>non-preemptive</strong>._

_<strong>All other</strong> scheduling are <strong>preemptive</strong>._

