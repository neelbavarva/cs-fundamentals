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

