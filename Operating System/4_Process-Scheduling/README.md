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

### Advantages of Preemptive Scheduling

- Preemptive scheduling method is more robust, approach so one process cannot monopolize the CPU
- Choice of running task reconsidered after each interruption.
- Each event cause interruption of running tasks
- The OS makes sure that CPU usage is the same by all running process.
- In this, the usage of CPU is the same, i.e., all the running processes will make use of CPU equally.
- This scheduling method also improvises the average response time.
- Preemptive Scheduling is beneficial when we use it for the multi-programming environment.

### Advantages of Non-preemptive Scheduling

- Offers low scheduling overhead
- Tends to offer high throughput
- It is conceptually very simple method
- Less computational resources need for Scheduling

### Disadvantages of Preemptive Scheduling

- Need limited computational resources for Scheduling
- Takes a higher time by the scheduler to suspend the running task, switch the context, and dispatch the new incoming task.
- The process which has low priority needs to wait for a longer time if some high priority processes arrive continuously.

### Disadvantages of Non-Preemptive Scheduling

- It can lead to starvation especially for those real-time tasks
- Bugs can cause a machine to freeze up
- It can make real-time and priority Scheduling difficult
- Poor response time for processes

<hr>

## Dispatcher

A dispatcher is a special program which comes into play after the scheduler. When the scheduler completes its job of selecting a process, it is the dispatcher which takes that process to the desired state/queue. The dispatcher is the module that gives a process control over the CPU after it has been selected by the short-term scheduler. This function involves the following:

- Switching context
- Switching to user mode
- Jumping to the proper location in the user program to restart that program

<strong>Dispatch latency</strong> is the time taken to stop a process and start another.

_Dispatch latency is a pure overhead._

## Scheduling Criteria

- ↑ CPU utilization - percentage
- ↑ Throughput - number of processes completed per unit time
- ↓ Turnaround time - time from submission to completion (time spent in different queues + time spent in CPU + time spent in different i/o devices)
- ↓ Waiting time - time spent in ready queue (only)
- ↓ Response time - time from submission to first response

## Scheduling Algorithms

- <strong>Arrival Time</strong> : Time at which the process arrives in the ready queue.
- <strong>Completion Time</strong> : Time at which process completes its execution.
- <strong>Burst Time</strong> : Time required by a process for CPU execution.
- <strong>Turn Around Time</strong> : Time Difference between completion time and arrival time.
- <strong>Turn Around Time</strong>  = Completion Time – Arrival Time
- <strong>Waiting Time(W.T)</strong> : Time Difference between turn around time and burst time.
- <strong>Waiting Time</strong> = Turn Around Time – Burst Time

<hr>

### First-come first-served (FCFS)

- non-preemptive
- high average waiting time
- convoy effect - several small processes may need to wait if a large process is given the CPU 
- Mode : Non-Preemptive
- Criteria : Arrival Time

### Shortest-job-first (SJF) scheduling

- process with the smallest next CPU burst is selected
- FCFS to break ties
- more appropriate term: shortest-next-CPU-burst-first
- optimal, but cannot be implemented 
- Criteria : Burst Time

_SJF can be either preemptive or non-preemptive._

<strong>Non-Preemptive</strong> = shortest-job-first

<strong>Preemptive SJF</strong> = shortest-remaining-time-first. 

### Priority scheduling

- CPU is allocated to the process with the highest priority
- priority range be 0 to 7 (say), with 0 representing the highest or the lowest priority
- priority may depend on internal factors (time limit, memory requirement, number of open
files, etc.) and external factors (user, department, etc.)
- may be preemptive or non-preemptive
- SJF is a special case of priority scheduling, with priority inversely proportional to predicted
next CPU burst length
- may cause starvation, i.e. indefinite blocking of processes
- aging: gradually increase the priority of a process waiting for a long time
- priority inversion: a low-priority process gets the priority of a high-priority process waiting
for it 

### Round robin (RR) scheduling

- a small time quantum or time slice is defined
- the ready queue is treated as a circular queue
- each process is allocated the CPU for one time quantum
- if time quantum is too large, then RR behaves like FCFS
- if time quantum is too small, then RR behaves like processor sharing
- rule of thumb: 80% CPU bursts should be shorter than the time quantum 
- Mode : Preemptive
- Criteria : Time Quantum

### Multilevel queue scheduling

- the ready queue is partitioned into several queues
- a process is permanently assigned to one queue
- each queue has its own scheduling algorithm
- inter-queue scheduling: preemptive priority scheduling or RR (80% time for foreground
processes and 20% time for background processes)

<img width=600 src="https://user-images.githubusercontent.com/62550592/149872248-b036d2a1-71c1-435a-8351-5c982ed47157.png" />

### Multilevel feedback queue scheduling

- allows processes to move between queues
- inter-queue scheduling: preemptive priority scheduling
- a process waiting too long in a low-priority queue may be moved to a high-priority queue 

<img width=500 src="https://user-images.githubusercontent.com/62550592/149872652-70fdc928-c966-4e5e-a717-cfac079e9dc0.png" />

![image](https://user-images.githubusercontent.com/62550592/149872786-a7707d90-43ff-43a0-83ef-043c5982aaec.png)

### Multiple processor scheduling

- multiprocessor systems: homogeneous or heterogeneous
- CPU scheduling approaches
    - asymmetric multiprocessing 
    - one processor performs scheduling for all
    - symmetric multiprocessing 
    - each processor is self-scheduling
    - e.g. Linux supports symmetric multiprocessing
- processor affinity –
    - because of high cost of invalidating and repopulating caches, migration of processes
      from one processor to another is avoided
    - attempt is made to keep a process at a given processor
    - hard- and soft- affinity
- load balancing –
    - attempt to keep all processors equally loaded
    - pull migration, push migration, combination
    - only for symmetric systems
    - counteracts the benefits of processor affinity 

<hr>

## Starvation

Starvation is the problem that occurs when high priority processes keep executing and low priority processes get blocked for indefinite time. In heavily loaded computer system, a steady stream of higher-priority processes can prevent a low-priority process from ever getting the CPU.

## Aging

Aging is a technique of gradually increasing the priority of processes that wait in the system for a long time.

For example, if priority range from 127(low) to 0(high), we could increase the priority of a waiting process by 1 Every 15 minutes. Eventually even a process with an initial priority of 127 would take no more than 32 hours for priority 127 process to age to a priority-0 process.

