## What is Networking?

Computer networking refers to connected computing devices (such as laptops, desktops, servers, smartphones, and tablets) and an ever-expanding array of IoT devices (such as cameras, door locks, doorbells, refrigerators, audio/visual systems, thermostats, and various sensors) that communicate with one another.

<hr>

## Basic Terms

### Client
A client is a computer hardware device or software that accesses a service made available by a server. The server is often (but not always) located on a separate physical computer.

### Server
A server is a physical computer dedicated to run services to serve the needs of other computers. Depending on the service that is running, it could be a file server, database server, home media server, print server, or web server.

### Host
A host is a computer, connected to other computers for which it provides data or services over a network. In theory, every computer connected to a network acts as a host to other peers on the network. In essence, a host reflects the logical relationship of two or more computers on a network. <br><br>
To simplify this, suppose you want to download an image from another computer on your network. That computer is “hosting” the image and therefore, it is the host computer. On the other hand, if that same computer downloads an image from your computer, your computer becomes the host computer.

### Q. Difference between a Server and a Host
A server:
- Can be a physical device or software program
- Installed on a host computer
- Provides specific services
- Serves only clients

A host:

- Is always a physical computer or device
- Can run both server and client programs
- Provides specific services
- Serves multiple users and devices

### Peer
A peer is something or someone that is an equal member of a group, where there's some kind of relationship between the members of the group.

<img src="https://i.stack.imgur.com/XPtvq.png" />

- Host 1, Layer 5 is a peer to Host 2, Layer 5.
- Host 1, Layer 4 is a peer to Host 2, Layer 4.
- Host 1, Layer 3 is a peer to Host 2, Layer 3.
- Host 1, Layer 2 is a peer to Host 2, Layer 2.
- Host 1, Layer 1 is a peer to Host 2, Layer 1.

### Bandwidth
Network bandwidth is a measurement indicating the maximum capacity of a wired or wireless communications link to transmit data over a network connection in a given amount of time. Typically, bandwidth is represented in the number of bits, kilobits, megabits or gigabits that can be transmitted in 1 second. Synonymous with capacity, bandwidth describes data transfer rate. Bandwidth is not a measure of network speed -- a common misconception.

### Jitter
Information is transported from your computer in data packets across the internet. They are usually sent at regular intervals and take a set amount of time. Jitter is when there is a time delay in the sending of these data packets over your network connection. This is often caused by network congestion, and sometimes route changes. <br>

Essentially, the longer data packets take to arrive, the more jitter can negatively impact the video and audio quality.

### Packets
A packet is a small segment of a larger message. Data sent over computer networks*, is divided into packets. These packets are then recombined by the computer or device that receives them.

### Frame 
In networking, a frame is a unit of data. A frame works to help identify data packets used in networking and telecommunications structures. Frames also help to determine how data receivers interpret a stream of data from a source. <br>

One way to define frames in networking is that the frame is a primary data unit within Level 2, or the data link layer of the OSI model. By contrast, Level 3, or the networking layer of the OSI model uses the packet as a primary data unit.<br>

Frames and packets may have different terminology attached to their use depending on the context or industry in question. In general, the frame is a formatting resource for data that needs to be split up into recognizable pieces in order to be interpreted by a receiver.

### Bit Rate
Network connections can send bits very fast. We measure that speed using the bit rate, the number of bits of data that are sent each second.

### Noise
Noise is any undesired signal in a communication circuit. Another definition calls noise unwanted disturbances superimposed on a useful signal, which tends to obscure its information content. There are many varieties of noise; however, the four most important to the telecommunication/data communication technologist are thermal noise, intermodulation noise, crosstalk and impulse noise.

### Attenuation
Attenuation is the loss of signal strength in networking cables or connections. This typically is measured in decibels (dB) or voltage and can occur due to a variety of factors. It may cause signals to become distorted or indiscernible. An example of this is Wi-Fi signal and strength getting noticeably weaker the further that your device is from the router. 

### Distortion
Distortion is a term used to describe an interruption of transmitting signals that cause an unclear reception. Distortion is commonly found in sound generated or received by a computer, video or display signals and data cables such as network cables.

<hr>

## What’s difference between The Internet and The Web ?
The Internet is a global network of networks while the Web, also referred formally as World Wide Web (www) is a collection of information that is accessed via the Internet. Another way to look at this difference is; the Internet is infrastructure while the Web is served on top of that infrastructure.

<hr>

## Types of Transmission Media
Transmission medium is a physical path between the transmitter and the receiver. Transmission Media is broadly classified into the following types:  
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20201030064943/TypesOfTransmissionMedia.jpg" />

<hr>

## Unicast, Broadcast and Multicast

### Unicast
- single sender and single recipient
- one-to-one transmission

### Broadcast
- one-to-one transmission

### Multicast
- one/more senders and one/more recipients participate
- in this method traffic recline between the boundaries of unicast (one-to-one) and broadcast (one-to-all)

<hr>

## Network Topology

Network topologies describe the methods in which all the elements of a network are mapped. The topology term refers to both the physical and logical layout of a network.

<img src="https://www.guru99.com/images/2/network_topology.png" />

### P2P
The network consists of a direct link between two computers

### Bus
Uses a single cable which connects all the included nodes

### Ring
Every device has exactly two neighboring devices for communication purpose

### Star
All the computers connect with the help of a hub.

### Mesh
The mesh topology has a unique network design in which each computer on the network connects to every other.

### Tree
Tree topologies have a root node, and all other nodes are connected which forming a hierarchy.

### Hybrid
Hybrid topology combines two or more topologies	.

<hr>

## LAN, MAN and WAN

### LAN
LAN stands for local area network. It is a group of network devices that allow communication between various connected devices. Private ownership has control over the local area network rather than the public. LAN has a short propagation delay than MAN as well as WAN. It covers the smaller area such as colleges, schools, hospitals, and so on. 

### MAN
MAN stands for metropolitan area network. It covers the larger area than LAN such as small towns, cities, etc. MAN connects two or more computers that reside within the same or completely different cities. MAN is expensive and should or might not be owned by one organization. 

### WAN
WAN stands for wide area network. It covers a large area than LAN as well as a MAN such as country/continent etc. WAN is expensive and should or might not be owned by one organization. PSTN or satellite medium is used for wide area networks. 

![image](https://user-images.githubusercontent.com/62550592/145455705-17ea35d1-39d2-4fdc-8bed-89c3eadb86ee.png)

