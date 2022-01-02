## What is Operating System

An operating system is a piece of software that manages all the resources of a computer system, both hardware and software, and provides an environment in which the user can execute his/her programs in a convenient and efficient manner. 

An operating system –
- manages the computer hardware
- facilitates execution of application programs
- acts as an intermediary between the user and the computer hardware
- designed to be convenient and efficient 

## Types of OS

### Batch Operating System

This type of operating system does not interact with the computer directly. There is an operator which takes similar jobs having the same requirement and group them into batches. It is the responsibility of the operator to sort jobs with similar needs. 

<img src="https://media.geeksforgeeks.org/wp-content/uploads/BatchOS.jpeg" />

### Time-Sharing Operating Systems

Each task is given some time to execute so that all the tasks work smoothly. Each user gets the time of CPU as they use a single system. These systems are also known as Multitasking Systems. The task can be from a single user or different users also. The time that each task gets to execute is called quantum. After this time interval is over OS switches over to the next task. 

<img src="https://media.geeksforgeeks.org/wp-content/uploads/Time-Share.jpeg" />

### Distributed Operating System

These types of the operating system is a recent advancement in the world of computer technology and are being widely accepted all over the world and, that too, with a great pace. Various autonomous interconnected computers communicate with each other using a shared communication network. Independent systems possess their own memory unit and CPU. These are referred to as loosely coupled systems or distributed systems. These system’s processors differ in size and function. The major benefit of working with these types of the operating system is that it is always possible that one user can access the files or software which are not actually present on his system but some other system connected within this network i.e., remote access is enabled within the devices connected in that network. 
 
<img src="https://media.geeksforgeeks.org/wp-content/uploads/Distributed.jpeg" />

### Network Operating System

These systems run on a server and provide the capability to manage data, users, groups, security, applications, and other networking functions. These types of operating systems allow shared access of files, printers, security, applications, and other networking functions over a small private network. One more important aspect of Network Operating Systems is that all the users are well aware of the underlying configuration, of all other users within the network, their individual connections, etc. and that’s why these computers are popularly known as tightly coupled systems. 

<img src="https://media.geeksforgeeks.org/wp-content/uploads/Network-OS.jpeg" />

### Real-Time Operating System

These types of OSs serve real-time systems. The time interval required to process and respond to inputs is very small. This time interval is called response time. 

Real-time systems are used when there are time requirements that are very strict like missile systems, air traffic control systems, robots, etc. 

<strong>Two types of Real-Time Operating System which are as follows: </strong>

<strong>Hard Real-Time Systems: </strong>

- These OSs are meant for applications where time constraints are very strict and even the shortest possible delay is not acceptable. These systems are built for saving life like automatic parachutes or airbags which are required to be readily available in case of any accident. Virtual memory is rarely found in these systems.

<strong>Soft Real-Time Systems: </strong>

- These OSs are for applications where for time-constraint is less strict.
 
## RAM vs ROM

<strong>RAM</strong> is Random Access Memory. The information stored in this type of memory is lost when the power supply to the PC or laptop is switched off. The information stored in RAM can be checked with the help of BIOS. It is generally known as the main memory, or temporary memory or cache memory or volatile memory of the computer system.

<strong>ROM</strong> is a Read-Only Memory. It is a permanent type of memory. Its content are not lost when the power supply is switched off. The computer manufacturer decides the information of ROM, and it is permanently stored at the time of manufacturing, which cannot be overwritten by the user.

## SRAM vs DRAM

<strong>SRAM</strong> is a type of semiconductor memory that uses Bistable latching circuitry to store each bit. In this type of RAM, data is stored using the six transistor memory cell. Static RAM is mostly used as a cache memory for the processor (CPU).

SRAM is relatively faster than other RAM types, such as DRAM. It also consumes less power. The full form of SRAM is Static Random Access Memory.

<strong>DRAM</strong> is a type of RAM which allows you to stores each bit of data in a separate capacitor within a particular integrated circuit.

It is a standard computer memory of any modern desktop computer. The full form of DRAM is Dynamic Random Access Memory.

DRAM is constructed using capacitors and a few transistors. In this type of RAM, the capacitor is used for storing the data where bit value, which signifies that the capacitor is charged and a bit value 0, which means that the capacitor is discharged.

## PROM, EPROM and EEPROM

The main difference between PROM EPROM and EEPROM is that PROM(Programmable Read Only Memory) is programmable only once while EPROM(Erasable Programmable Read Only Memory) is reprogrammable using ultraviolet light and EEPROM(Electrically Erasable Programmable Read-Only Memory) is reprogrammable using an electric charge.

## Virtualization and Containerization

<strong>Virtualization</strong> is the technology which can simulate your physical hardware (such as CPU cores, memory, disk)  and represent it as seperate machine. It has its own Guest OS, Kernel, process, drivers and  etc. Therefore, it is hardware level virtualization. Most common technology is VMware and VirtualBox

<strong>Containerization</strong> is os-level virtualization. It doesn't simulate the entire physical machine. It just simulate the OS of your machine. Therefore multiple applications can share the same OS kernel. Container play similar roles to virtual machine but without hardware virtualization.  Most common container technology is Docker

## UEFI and BIOS

Both UEFI(Unified Extensible Firmware Interface) and BIOS(Basic Input-Output system) are low-level software that starts when you boot your PC before booting your operating system, but UEFI is a more modern solution, supporting larger hard drives, faster boot times, more security features, and—conveniently—graphics and mouse cursors.

BIOS is low-level software that resides in a chip on your computer’s motherboard. The BIOS loads when your computer starts up, and the BIOS is responsible for waking up your computer’s hardware components, ensures they’re functioning properly, and then runs the bootloader that boots Windows or whatever other operating system you have installed.


