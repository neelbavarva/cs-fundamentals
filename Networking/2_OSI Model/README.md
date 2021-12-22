## What is OSI Model?
OSI(Open System Interconnection) : The purpose of the OSI model is to facilitate communication between different systems without requiring changes to the logic of the underlying hardware and software.

## Different layers in OSI Model

Physical -> Data Link -> Network -> Transport -> Session -> Presentation -> Application

<div align="left">
  <img height=400 src="https://www.tutorialandexample.com/wp-content/uploads/2020/10/image-201.png" />
  <img height=400 src="https://media.geeksforgeeks.org/wp-content/uploads/computer-network-osi-model-layers.png" />
</div>

## Physical Layer

The lowest layer of the OSI reference model is the physical layer. It is responsible for the actual physical connection between the devices. The physical layer contains information in the form of bits. It is responsible for transmitting individual bits from one node to the next. When receiving data, this layer will get the signal received and convert it into 0s and 1s and send them to the Data Link layer, which will put the frame back together.

The functions of the physical layer are :  

<strong>1. Bit synchronization</strong> : The physical layer provides the synchronization of the bits by providing a clock. This clock controls both sender and receiver thus providing synchronization at bit level.

<strong>2. Bit rate control</strong> : The Physical layer also defines the transmission rate i.e. the number of bits sent per second.

<strong>3. Physical topologies</strong> : Physical layer specifies the way in which the different, devices/nodes are arranged in a network i.e. bus, star, or mesh topology.

<strong>4. Transmission mode</strong> : Physical layer also defines the way in which the data flows between the two connected devices. The various transmission modes possible are Simplex, half-duplex and full-duplex.

## Data Link Layer

The data link layer is responsible for the node-to-node delivery of the message. The main function of this layer is to make sure data transfer is error-free from one node to another, over the physical layer. When a packet arrives in a network, it is the responsibility of DLL to transmit it to the Host using its MAC address.

Data Link Layer is divided into two sublayers:  

<strong>1. Logical Link Control (LLC)</strong><br>
<strong>2. Media Access Control (MAC)</strong>

The packet received from the Network layer is further divided into frames depending on the frame size of NIC(Network Interface Card). DLL also encapsulates Sender and Receiver’s MAC address in the header. 

The functions of the Data Link layer are :  

<strong>1. Framing</strong> : Framing is a function of the data link layer. It provides a way for a sender to transmit a set of bits that are meaningful to the receiver. This can be accomplished by attaching special bit patterns to the beginning and end of the frame.

<strong>2. Physical addressing</strong> : After creating frames, the Data link layer adds physical addresses (MAC address) of the sender and/or receiver in the header of each frame.

<strong>3. Error control</strong> : Data link layer provides the mechanism of error control in which it detects and retransmits damaged or lost frames.

<strong>4. Flow Control</strong> : The data rate must be constant on both sides else the data may get corrupted thus, flow control coordinates the amount of data that can be sent before receiving acknowledgement.

<strong>5. Access control</strong> : When a single communication channel is shared by multiple devices, the MAC sub-layer of the data link layer helps to determine which device has control over the channel at a given time.

*** _Packet in Data Link layer is referred to as Frame. <br>
*** Data Link layer is handled by the NIC (Network Interface Card) and device drivers of host machines. <br>
*** Switch & Bridge are Data Link Layer devices._

<a href="https://www.geeksforgeeks.org/flow-control-in-data-link-layer/">Flow Control in Data Link Layer</a>

<hr>

### What Is Ethernet?

Ethernet is the most widely used LAN technology, which is defined under IEEE standards 802.3. The reason behind its wide usability is Ethernet is easy to understand, implement, maintain, and allows low-cost network implementation. Also, Ethernet offers flexibility in terms of topologies that are allowed. Ethernet generally uses Bus Topology. Ethernet operates in two layers of the OSI model, Physical Layer, and Data Link Layer. For Ethernet, the protocol data unit is Frame since we mainly deal with DLL. In order to handle collision, the Access control mechanism used in Ethernet is CSMA/CD. Manchester Encoding Technique is used in Ethernet. 

### Difference between Internet, Intranet and Extranet

<strong>1. Internet</strong> : The network formed by the co-operative interconnection of millions of computers, linked together is called Internet.

<strong>2. Intranet</strong> : It is an internal private network built within an organization using Internet and World Wide Web standards and products that allows employees of an organization to gain access to corporate information. 

<strong>3. Extranet</strong> : It is the type of network that allows users from outside to access the Intranet of an organization. 

### Virtual Circuits and Datagram Networks

Computer networks that provide connection-oriented services are called Virtual Circuits while those providing connection-less services are called Datagram networks. For prior knowledge, the Internet which we use is actually based on a Datagram network (connection-less) at the network level as all packets from a source to a destination do not follow the same path. 

### Virtual LAN

VLAN is a custom network which is created from one or more local area networks. It enables a group of devices available in multiple networks to be combined into one logical network. The result becomes a virtual LAN that is administered like a physical LAN. The full form of VLAN is defined as Virtual Local Area Network. VLAN in networking is a virtual extension of LAN

The below topology depicts a network having all hosts inside the same virtual LAN:

<img src="https://www.guru99.com/images/2/100720_0948_WhatisVLANT1.png" />

### Wi-Fi

Wi-Fi stands for Wireless Fidelity. It is a technology for wireless local area networking with devices based on IEEE 802.11 standards. Wi-Fi compatible devices can connect to the internet via WLAN network and a wireless access point abbreviated as AP. Wired networks differ from wireless which uses radio waves rather than transmitting electrical signals over the cables.

<hr>

## Network Layer

The network layer works for the transmission of data from one host to the other located in different networks. It also takes care of packet routing i.e. selection of the shortest path to transmit the packet, from the number of routes available. The sender & receiver’s IP addresses are placed in the header by the network layer. 

The functions of the Network layer are :  

<strong>1. Routing :</strong> The network layer protocols determine which route is suitable from source to destination. This function of the network layer is known as routing.

<strong>2. Logical Addressing :</strong> In order to identify each device on internetwork uniquely, the network layer defines an addressing scheme. The sender & receiver’s IP addresses are placed in the header by the network layer. Such an address distinguishes each device uniquely and universally.

<hr>

### IP Address

An IP address is a unique address that identifies a device on the internet or a local network. IP stands for "Internet Protocol," which is the set of rules governing the format of data sent via the internet or local network.

In essence, IP addresses are the identifier that allows information to be sent between devices on a network: they contain location information and make devices accessible for communication. The internet needs a way to differentiate between different computers, routers, and websites. IP addresses provide a way of doing so and form an essential part of how the internet works.

![image](https://user-images.githubusercontent.com/62550592/146629822-b9a2be42-ee8b-4c11-adc0-083df9a0969b.png)

### IPv4 vs IPv6

IPv4 is an IP version widely used to identify devices on a network using an addressing system. It was the first version of IP deployed for production in the ARPANET in 1983. It uses a 32-bit address scheme to store 2^32 addresses which is more than 4 billion addresses. It is considered the primary Internet Protocol and carries 94% of Internet traffic.

IPv6 is the most recent version of the Internet Protocol. This new IP address version is being deployed to fulfill the need for more Internet addresses. It was aimed to resolve issues that are associated with IPv4. With 128-bit address space, it allows 340 undecillion unique address space. IPv6 is also called IPng (Internet Protocol next generation).

![image](https://user-images.githubusercontent.com/62550592/146630017-409a0718-201d-45b3-8dd1-05b6c23ab256.png)

<img src="https://www.guru99.com/images/1/053018_0657_IPv4vsIPv6W1.png" />

### Supernet

Supernetting is the opposite of Subnetting. In subnetting, a single big network is divided into multiple smaller subnetworks. In Supernetting, multiple networks are combined into a bigger network termed as a Supernetwork or Supernet. 

### Routing 

Routing is a process that is performed by layer 3 (or network layer) devices in order to deliver the packet by choosing an optimal path from one network to another. 

<strong>1. Static Routing : </strong> Static routing is a process in which we have to manually add routes to the routing table. 

<strong>2. Defaulr Routing : </strong> This is the method where the router is configured to send all packets towards a single router (next hop). It doesn’t matter to which network the packet belongs, it is forwarded out to the router which is configured for default routing. It is generally used with stub routers. A stub router is a router that has only one route to reach all other networks. 

<strong>3. Dynamic Routing : </strong> Dynamic routing makes automatic adjustments of the routes according to the current state of the route in the routing table. Dynamic routing uses protocols to discover network destinations and the routes to reach them. RIP and OSPF are the best examples of dynamic routing protocols. Automatic adjustments will be made to reach the network destination if one route goes down. 

### NAT

To access the Internet, one public IP address is needed, but we can use a private IP address in our private network. The idea of NAT is to allow multiple devices to access the Internet through a single public address. To achieve this, the translation of a private IP address to a public IP address is required. Network Address Translation (NAT) is a process in which one or more local IP address is translated into one or more Global IP address and vice versa in order to provide Internet access to the local hosts. Also, it does the translation of port numbers i.e. masks the port number of the host with another port number, in the packet that will be routed to the destination. It then makes the corresponding entries of IP address and port number in the NAT table. NAT generally operates on a router or firewall. 

### WPA & WPS

WPS stands for wifi protected setup. wifi devices usually require a bit of tweaking before they can be set up. You need to configure an SSID, take care of the security of the network by assigning it a password and then you need to connect it with your client, where the steps are repeated. Although this method is usually required only once still it was considered to be a bit of a hassle.

WPA stands for wireless protected access. WPA 2 psk is a variant of WPA where the key is shared between connected devices. PSK here stands for pre shared key. WPA 2 psk is designed for a small office and home network where all the people who'll be connecting to wifi can be trusted. Although WPA 2 is secure sharing the password with other people means that any one who has access to it can snoop on the network. For a home use case a WPA-2 psk is secure enough. And you can always change the password if you have any doubts that some one else is using it.

### LiFi and WiFi

Wi-Fi(wireless fidelity) and Li-Fi(light fidelity) both are two different technologies which are used to send and receive data wirelessly. In case of Wi-Fi we use Routers and Radio Frequency (RF) waves to transmit data, whereas in Li-Fi we use LED bulbs and Light signals to transmit and receive data.

### Access-Lists (ACL)

Access-list (ACL) is a set of rules defined for controlling network traffic and reducing network attacks. ACLs are used to filter traffic based on the set of rules defined for the incoming or outgoing of the network. 

### AAA (Authentication, Authorization and Accounting)

AAA is a standard-based framework used to control who is permitted to use network resources (through authentication), what they are authorized to do (through authorization), and capture the actions performed while accessing the network (through accounting). 

<strong>1. Authentication : </strong>The process by which it can be identified that the user, which wants to access the network resources, valid or not by asking some credentials such as username and password. Common methods are to put authentication on console port, AUX port, or vty lines. 

As network administrators, we can control how a user is authenticated if someone wants to access the network. Some of these methods include using the local database of that device (router) or sending authentication requests to an external server like the ACS server. To specify the method to be used for authentication, a default or customized authentication method list is used. 

<strong>2. Authorization : </strong>It provides capabilities to enforce policies on network resources after the user has gained access to the network resources through authentication. After the authentication is successful, authorization can be used to determine what resources is the user allowed to access and the operations that can be performed. 

For example, if a junior network engineer (who should not access all the resources) wants to access the device then the administrator can create a view that will allow particular commands only to be executed by the user (the commands that are allowed in the method list). The administrator can use the authorization method list to specify how the user is authorized to network resources i.e through a local database or ACS server. 

<strong>3. Accounting : </strong> It provides means of monitoring and capturing the events done by the user while accessing the network resources. It even monitors how long the user has access to the network. The administrator can create an accounting method list to specify what should be accounted for and to whom the accounting records should be sent. 

![image](https://user-images.githubusercontent.com/62550592/146647219-0ec480d4-8208-4bd5-ab50-254e39386e15.png)

### Synchronous Optical Network (SONET)

SONET stands for Synchronous Optical Network. SONET is a communication protocol, developed by Bellcore – that is used to transmit a large amount of data over relatively large distances using optical fibre. With SONET, multiple digital data streams are transferred at the same time over the optical fibre.

<hr>

## Transport Layer

The transport layer provides services to the application layer and takes services from the network layer. The data in the transport layer is referred to as Segments. It is responsible for the End to End Delivery of the complete message. The transport layer also provides the acknowledgement of the successful data transmission and re-transmits the data if an error is found. 

<strong>* At sender's side</strong> 
Transport layer receives the formatted data from the upper layers, performs Segmentation, and also implements Flow & Error control to ensure proper data transmission. It also adds Source and Destination port numbers in its header and forwards the segmented data to the Network Layer. 

<strong>* At receiver's side</strong>
Transport Layer reads the port number from its header and forwards the Data which it has received to the respective application. It also performs sequencing and reassembling of the segmented data. 

![image](https://user-images.githubusercontent.com/62550592/146683646-550206c3-5298-4672-9973-a8b7c84a4cdd.png)

![image](https://user-images.githubusercontent.com/62550592/146683614-04039e7c-2671-42be-b26e-e130faceb2ca.png)

<hr>

### TCP 3-Way Handshake Process

The two important protocols of this layer are – TCP, UDP(User Datagram Protocol) out of which TCP is prevalent(since it provides reliability for the connection established). An application of UDP in querying the DNS server to get the binary equivalent of the Domain Name used for the website.

TCP provides reliable communication with something called Positive Acknowledgement with Re-transmission(PAR). The Protocol Data Unit(PDU) of the transport layer is called a segment. Now a device using PAR resend the data unit until it receives an acknowledgement. If the data unit received at the receiver’s end is damaged(It checks the data with checksum functionality of the transport layer that is used for Error Detection), the receiver discards the segment. So the sender has to resend the data unit for which positive acknowledgement is not received. You can realize from the above mechanism that three segments are exchanged between sender(client) and receiver(server) for a reliable TCP connection to get established. 

![image](https://user-images.githubusercontent.com/62550592/146684503-fac46bb8-da21-4981-8969-c4243ba6712c.png)

### P2P(Peer To Peer) File Sharing

The individual users in the network(file sharing network) are referred to as peers. The peers request files from other peers by establishing TCP or UDP connections. 

Now, when one peer makes a request, it is possible that multiple peers have a copy of that requested object. Now the problem is how to get the IP addresses of all those peers. This is decided by the underlying architecture supported by the P2P systems. By means of one of these methods, the client peer can get to know about all the peers which have the requested object/file and the file transfer takes place directly between these two peers. 

![image](https://user-images.githubusercontent.com/62550592/146684833-927becf9-e02f-482b-9246-48fcc936029c.png)

![image](https://user-images.githubusercontent.com/62550592/146684860-35d4b735-0d72-4637-9ab7-656875f64aa6.png)

![image](https://user-images.githubusercontent.com/62550592/146684892-949a9e7b-2d13-4e7b-9691-08345c7c5263.png)

### Congestion Control

A state occurs in the network layer when the message traffic is so heavy that it slows down network response time. Token bucket is superior to Leaky bucket

### Error Control

Error control in TCP is mainly done through the use of three simple techniques : 

![image](https://user-images.githubusercontent.com/62550592/146799219-60a3777f-46e1-4239-92b1-9ddf32bebdd9.png)

<hr>

## Session Layer

This layer is responsible for the establishment of connection, maintenance of sessions, authentication, and also ensures security. 

The functions of the session layer are :  

<strong>1. Session establishment, maintenance, and termination: </strong> The layer allows the two processes to establish, use and terminate a connection.

<strong>2. Synchronization: </strong> This layer allows a process to add checkpoints which are considered synchronization points into the data. These synchronization points help to identify the error so that the data is re-synchronized properly, and ends of the messages are not cut prematurely and data loss is avoided.

<strong>3. Dialog Controller: </strong>  The session layer allows two systems to start communication with each other in half-duplex or full-duplex.

## Presentation Layer

The presentation layer is also called the Translation layer. The data from the application layer is extracted here and manipulated as per the required format to transmit over the network. 

The functions of the presentation layer are : 

<strong>Translation: </strong> For example, ASCII to EBCDIC.

<strong>Encryption/ Decryption: </strong> Data encryption translates the data into another form or code. The encrypted data is known as the ciphertext and the decrypted data is known as plain text. A key value is used for encrypting as well as decrypting data.

<strong>Compression: </strong> Reduces the number of bits that need to be transmitted on the network.

## Application Layer

At this layer, both the end user and the application layer interact directly with the software application. This layer sees network services provided to end-user applications such as a web browser or Office 365.

<hr>

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

<img src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/gq/2017/02/DNS_2.png" />

<h4>Hierarchy of Name Servers</h4>

<h5>1. Root name servers</h5> 

It is contacted by name servers that can not resolve the name. It contacts authoritative name server if name mapping is not known. It then gets the mapping and return the IP address to the host.

<h5>2. Top level server</h5> 

It is responsible for com, org, edu etc and all top level country domains like uk, fr, ca, in etc. They have info about authoritative domain servers and know names and IP addresses of each authoritative name server for the second level domains.

<h5>3. Authoritative name servers</h5> 

This is organization’s DNS server, providing authoritative hostName to IP mapping for organization servers. It can be maintained by organization or service provider. In order to reach cse.dtu.in we have to ask the root DNS server, then it will point out to the top level domain server and then to authoritative domain name server which actually contains the IP address. So the authoritative domain server will return the associative ip address.

<img src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/gq/2017/02/DNS_3.png" />

The client machine sends a request to the local name server, which , if root does not find the address in its database, sends a request to the root name server , which in turn, will route the query to an intermediate or authoritative name server. The root name server can also contain some hostName to IP address mappings . The intermediate name server always knows who the authoritative name server is. So finally the IP address is returned to the local name server which in turn returns the IP address to the host.

### Why does DNS use UDP and not TCP?

DNS is an application layer protocol. All application layer protocols use one of the two transport layer protocols, UDP(User Datagram Protocol) and TCP(Transmission Control Protocol). TCP is reliable and UDP is not reliable. DNS is supposed to be reliable, but it uses UDP, why? 

There are the following interesting facts about TCP and UDP on the transport layer that justify the above.
1. UDP is much faster. TCP is slow as it requires a 3-way handshake. The load on DNS servers is also an important factor. DNS servers (since they use UDP) don’t have to keep connections. 
2. DNS requests are generally very small and fit well within UDP segments. 
3. UDP is not reliable, but reliability can be added to the application layer. An application can use UDP and can be reliable by using a timeout and resend at the application layer. 

Actually, DNS primarily uses the User Datagram Protocol (UDP) on port number 53 to serve requests. DNS queries consist of a single UDP request from the client followed by a single UDP reply from the server. When the length of the answer exceeds 512 bytes and both client and server support EDNS, larger UDP packets are used. Otherwise, the query is sent again using the Transmission Control Protocol (TCP). TCP is also used for tasks such as zone transfers. Some resolver implementations use TCP for all queries. 

### Address Resolution in DNS

In order to find a particular DNS requesting host place its query to the Local DNS Server with a mapping request. If it has the information, the resolver is satisfied else the resolver is referred to other servers or other servers are asked to provide the information. After the resolver, gets the response, it checks whether the response is correct or not. If the response is correct, the response is passed to the process that requested it, else the name query fails. 

A resolution can be of two types – iterative and recursive. 

<strong>1. Recursive :</strong> Here, the client requires the Local Server to give either the requested mapping or an error message. A DNS Query is generated by the application program to the resolver to fetch the destination IP Address. The Query is then forward to the local DNS Server. If it knows the IP Address, it sends a response to the resolver. Assuming, it does not know the IP Address, it sends the query to the root name server. 

The root name server contains information about at least one server of Top Level Domain. The query is then sent to the respective Top-Level Domain server. If it contains the mapping, the response is sent back to the root server and then to the host’s local server. If it doesn’t contain the mapping, it should contain the IP Address of the destination’s local DNS Server. The local DNS server knows the destination host’s IP Address. The information is then sent back to the top-level domain server, then to the root server and then to the host’s Local DNS Server, and finally to the host. 

<img src="https://media.geeksforgeeks.org/wp-content/uploads/222-1.jpg" />

<strong>2. Iterative :</strong> The main difference between iterative and recursive resolution is that here each server that does not know the mapping sends the IP Address of the next server to the one requested it. Here, the client allows the server to return the best answer it can give as a match or as a referral. A DNS Query is generated by the application program to the resolver to fetch the destination IP Address. The Query is then forward to the local DNS Server. Assuming, it does not know the IP Address, it sends the query to the root name server. 

The root name server returns the IP Address of the Top-Level Domain Server to the Local Server. The Top-Level Domain server is contacted by the Local Server and it returns either the IP of the destination host or its local DNS Server. If it returns the server’s address, then by contacting the destination’s Local DNS Server, we get the IP Address of the destination host. The response/mapping is then passed from the host’s local DNS server to the resolver and then finally to the host. 

<strong>Cashing Mechanism :</strong> In both iterative and recursive resolution, after a server asks for a mapping request from another server, it receives the response and stores this information in the Cache memory before sending it to the client. This is done to lower the search time it takes for a server to check the IP Address in its Database. So, the next time, if a request comes to the server, it first checks its cache memory and tries to resolve the request. The response is marked as Unauthoritative to inform the client that the response is from Cache. The only way caching can be problematic is when the server caches the mapping for a long time and the mapping gets outdated. However, there are techniques to resolve this like using TTL.

### DNS Spoofing or DNS Cache poisoning

DNS Spoofing means getting a wrong entry or IP address of the requested site from the DNS server. Attackers find out the flaws in the DNS system and take control and will redirect to a malicious website. 

<img src="https://media.geeksforgeeks.org/wp-content/uploads/DNS_Spoofing.png" />

### Types of DNS Attacks

<strong>1. Denial of service (DoS) :</strong> An attack where the attacker renders a computer useless (inaccessible) to the user by making a resource unavailable or by flooding the system with traffic.

<strong>2. Distributed denial of service (DDoS) :</strong> The attacker controls an overwhelming amount of computers (hundreds or thousands) in order to spread malware and flood the victim’s computer with unnecessary and overloading traffic. Eventually, unable to harness the power necessary to handle the intensive processing, the systems will overload and crash.

<strong>3. DNS spoofing (also known as DNS cache poisoning) :</strong> An attacker will drive the traffic away from real DNS servers and redirect them to a “pirate” server, unbeknownst to the users. This may cause the corruption/theft of a user’s personal data.

<strong>4. Fast flux :</strong> An attacker will typically spoof his IP address while performing an attack. Fast flux is a technique to constantly change location-based data in order to hide where exactly the attack is coming from. This will mask the attacker’s real location, giving him the time needed to exploit the attack. Flux can be single or double or of any other variant. A single flux changes the address of the webserver while double flux changes both the address of the web server and the names of DNS serves.

<strong>5. Reflected attacks :</strong> Attackers will send thousands of queries while spoofing their own IP address and using the victim’s source address. When these queries are answered, they will all be redirected to the victim himself.

<strong>6. Reflective amplification DoS :</strong> When the size of the answer is considerably larger than the query itself, a flux is triggered, causing an amplification effect. This generally uses the same method as a reflected attack, but this attack will overwhelm the user’s system’s infrastructure further.

### How DHCP server dynamically assigns IP address to a host?

DHCP is an abbreviation for Dynamic Host Configuration Protocol. It is an application layer protocol used by hosts for obtaining network setup information. The DHCP is controlled by a DHCP server that dynamically distributes network configuration parameters such as IP addresses, subnet masks, and gateway addresses. 

<a href="https://www.geeksforgeeks.org/how-dhcp-server-dynamically-assigns-ip-address-to-a-host/" >Read More</a>

<hr>
