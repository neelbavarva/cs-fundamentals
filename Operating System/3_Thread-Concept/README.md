## Threads

Thread is an execution unit that consists of its own program counter, a stack, and a set of registers where the program counter mainly keeps track of which instruction to execute next, a set of registers mainly hold its current working variables, and a stack mainly contains the history of execution

Threads are also known as Lightweight processes. Threads are a popular way to improve the performance of an application through parallelism. Threads are mainly used to represent a software approach in order to improve the performance of an operating system just by reducing the overhead thread that is mainly equivalent to a classical process.

The CPU switches rapidly back and forth among the threads giving the illusion that the threads are running in parallel.

As each thread has its own independent resource for process execution; thus Multiple processes can be executed parallelly by increasing the number of threads.

<strong>User threads</strong> are above the kernel and without kernel support. These are the threads that application programmers use in their programs.

<strong>Kernel threads</strong> are supported within the kernel of the OS itself. All modern OSs support kernel-level threads, allowing the kernel to perform multiple simultaneous tasks and/or to service multiple kernel system calls simultaneously.

## Benefits of Multithreading

<strong>1. Responsiveness</strong> : Multithreading in an interactive application may allow a program to continue running even if a part of it is blocked or is performing a lengthy operation, thereby increasing responsiveness to the user.

<strong>2. Resource Sharing</strong> : Processes may share resources only through techniques such as-
- Message Passing
- Shared Memory

Such techniques must be explicitly organized by programmer. However, threads share the memory and the resources of the process to which they belong by default.

The benefit of sharing code and data is that it allows an application to have several threads of activity within same address space.

<strong>3. Economy</strong> : Allocating memory and resources for process creation is a costly job in terms of time and space.
Since, threads share memory with the process it belongs, it is more economical to create and context switch threads. Generally much more time is consumed in creating and managing processes than in threads.

<strong>4. Scalability</strong> : The benefits of multi-programming greatly increase in case of multiprocessor architecture, where threads may be running parallel on multiple processors. If there is only one thread then it is not possible to divide the processes into smaller tasks that different processors can perform.

Single threaded process can run only on one processor regardless of how many processors are available.

Multi-threading on a multiple CPU machine increases parallelism.

## Example of Multithreading

1. Web Browsers - A web browser can download any number of files and web pages (multiple tabs) at the same time and still lets you continue browsing. If a particular web page cannot be downloaded, that is not going to stop the web browser from downloading other web pages.
2. Web Servers - A threaded web server handles each request with a new thread. There is a thread pool and every time a new request comes in, it is assigned to a thread from the thread pool.
3. Computer Games - You have various objects like cars, humans, birds which are implemented as separate threads. Also playing the background music at the same time as playing the game is an example of multithreading.
4. Text Editors - When you are typing in an editor, spell-checking, formatting of text and saving the text are done concurrently by multiple threads. The same applies for Word processors also.
5. IDE - IDEs like Android Studio run multiple threads at the same time. You can open multiple programs at the same time. It also gives suggestions on the completion of a command which is a separate thread.

## Multithreading Models

- Many to One Model
- One to One Model
- Many to Many Model

### Many To One Model 

- In the many to one model, many user-level threads are all mapped onto a single kernel thread.
- Thread management is handled by the thread library in user space, which is efficient in nature.
- In this case, if user-level thread libraries are implemented in the operating system in some way that the system does not support them, then the Kernel threads use this many-to-one relationship model.

### One to One Model

- The one to one model creates a separate kernel thread to handle each and every user thread.
- Most implementations of this model place a limit on how many threads can be created.
- Linux and Windows from 95 to XP implement the one-to-one model for threads.
- This model provides more concurrency than that of many to one Model.

### Many to Many Model

- The many to many model multiplexes any number of user threads onto an equal or smaller number of kernel threads, combining the best features of the one-to-one and many-to-one models.
- Users can create any number of threads.
- Blocking the kernel system calls does not block the entire process.
- Processes can be split across multiple processors.

## Optimal number of threads per core

If your threads don't do I/O, synchronization, etc., and there's nothing else running, 1 thread per core will get you the best performance. However that very likely not the case. Adding more threads usually helps, but after some point, they cause some performance degradation.

_Not long ago, I was doing performance testing on a 2 quad-core machine running an ASP.NET application on Mono under a pretty decent load. We played with the minimum and maximum number of threads and in the end we found out that for that particular application in that particular configuration the best throughput was somewhere <strong>between 36 and 40 threads</strong>. Anything outside those boundaries performed worse._

One thing for sure: 4k threads will take longer. That's a lot of context switches.
