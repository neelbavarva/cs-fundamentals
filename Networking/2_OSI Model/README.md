## What is OSI Model?
OSI(Open System Interconnection) : The purpose of the OSI model is to facilitate communication between different systems without requiring changes to the logic of the underlying hardware and software.

## Different layers in OSI Model

Physical -> Data Link -> Network -> Transport -> Session -> Presentation -> Application

<img src="https://www.tutorialandexample.com/wp-content/uploads/2020/10/image-201.png" />

## Application Layer

At this layer, both the end user and the application layer interact directly with the software application. This layer sees network services provided to end-user applications such as a web browser or Office 365.

### Protocols in Application Layer

<h5> 1. TELNET </h5>

Telnet stands for the TELetype NETwork. It helps in terminal emulation. It allows Telnet clients to access the resources of the Telnet server. It is used for managing files on the internet. It is used for the initial setup of devices like switches. The telnet command is a command that uses the Telnet protocol to communicate with a remote device or system. Port number of telnet is 23. 

```
telnet [\\RemoteServer]
\\RemoteServer   : Specifies the name of the server to which you want to connect
```

<h5> 2. FTP </h5>

FTP stands for file transfer protocol. It is the protocol that actually lets us transfer files. It can facilitate this between any two machines using it. But FTP is not just a protocol but it is also a program. FTP promotes sharing of files via remote computers with reliable and efficient data transfer. The Port number for FTP is 20 for data and 21 for control.

```
ftp machinename
```

<h5> 3. TFTP </h5>

The Trivial File Transfer Protocol (TFTP) is the stripped-down, stock version of FTP, but it’s the protocol of choice if you know exactly what you want and where to find it. It’s a technology for transferring files between network devices and is a simplified version of FTP. The Port number for TFTP is 69.

```
tftp [ options... ] [host [port]] [-c command] 
```

<h5> 4. NFS </h5>

It stands for a network file system. It allows remote hosts to mount file systems over a network and interact with those file systems as though they are mounted locally. This enables system administrators to consolidate resources onto centralized servers on the network. The Port number for NFS is 2049.

```
service nfs start
```

<h5> 5. SMTP </h5>

It stands for Simple Mail Transfer Protocol. It is a part of the TCP/IP protocol. Using a process called “store and forward,” SMTP moves your email on and across networks. It works closely with something called the Mail Transfer Agent (MTA) to send your communication to the right computer and email inbox. The Port number for SMTP is 25. 

```
MAIL FROM:<mail@abc.com?
```

<h5> 6. LPD </h5>

It stands for Line Printer Daemon. It is designed for printer sharing. It is the part that receives and processes the request. A “daemon” is a server or agent. The Port number for LPD is 515. 

```
lpd [ -d ] [ -l ] [ -D DebugOutputFile]
```

<h5> 7. X window </h5>

It defines a protocol for the writing of graphical user interface–based client/server applications. The idea is to allow a program, called a client, to run on one computer. It is primarily used in networks of interconnected mainframes. Port number for X window starts from 6000 and increases by 1 for each server.

```
Run xdm in runlevel 5 
```

<h5> 8. SNMP </h5>

It stands for Simple Network Management Protocol. It gathers data by polling the devices on the network from a management station at fixed or random intervals, requiring them to disclose certain information. It is a way that servers can share information about their current state, and also a channel through which an administrate can modify pre-defined values. The Port number of SNMP is 161(TCP) and 162(UDP). 

```
snmpget -mALL -v1 -cpublic snmp_agent_Ip_address sysName.0
```

<h5> 9. DNS </h5>

It stands for Domain Name System. Every time you use a domain name, therefore, a DNS service must translate the name into the corresponding IP address. For example, the domain name www.abc.com might translate to 198.105.232.4. 
The Port number for DNS is 53. 

```
ipconfig /flushdns
```

<h5> 10. DHCP </h5>

It stands for Dynamic Host Configuration Protocol (DHCP). It gives IP addresses to hosts. There is a lot of information a DHCP server can provide to a host when the host is registering for an IP address with the DHCP server. Port number for DHCP is 67, 68. 

```
clear ip dhcp binding {address | * }
```

### DNS

DNS is a host name to IP address translation service. DNS is a distributed database implemented in a hierarchy of name servers.

Every host is identified by the IP address but remembering numbers is very difficult for the people and also the IP addresses are not static therefore a mapping is required to change the domain name to IP address. So DNS is used to convert the domain name of the websites to their numerical IP address.

<h4>Domain:</h4>

1. Generic domain : .com(commercial) .edu(educational) .mil(military) .org(non profit organization) .net(similar to commercial) all these are generic domain.
2. Country domain .in (india) .us .uk
3. Inverse domain if we want to know what is the domain name of the website. Ip to domain name mapping.So DNS can provide both the mapping for example to find the ip addresses of geeksforgeeks.org then we have to type nslookup www.geeksforgeeks.org.

