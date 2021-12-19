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

## Transport Layer

The transport layer provides services to the application layer and takes services from the network layer. The data in the transport layer is referred to as Segments. It is responsible for the End to End Delivery of the complete message. The transport layer also provides the acknowledgement of the successful data transmission and re-transmits the data if an error is found. 

<strong>* At sender's side</strong> 
Transport layer receives the formatted data from the upper layers, performs Segmentation, and also implements Flow & Error control to ensure proper data transmission. It also adds Source and Destination port numbers in its header and forwards the segmented data to the Network Layer. 

<strong>* At receiver's side</strong>
Transport Layer reads the port number from its header and forwards the Data which it has received to the respective application. It also performs sequencing and reassembling of the segmented data. 

<hr>
