## Process Scheduling

Process Scheduling is an OS task that schedules processes of different states like ready, waiting, and running. Process scheduling allows OS to allocate a time interval of CPU execution for each process. Another important reason for using a process scheduling system is that it keeps the CPU busy all the time. This allows you to get the minimum response time for programs.

## CPU Burst and I/O Burst

Burst is the amount of time required by a process or can be said the amount of time required by the process to finish.

A CPU bursts when it is executing instructions; an I/O system bursts when it services requests to fetch information. The idea is that each component operates until it can’t.

A CPU can run instructions from cache until it needs to fetch more instructions or data from memory. That ends the CPU burst and starts the I/O burst. The I/O burst read or writes data until the requested data is read/written or the space to store it cache runs out. That ends an I/O burst.
