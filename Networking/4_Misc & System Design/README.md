## Common Networking Commands

<a href="https://www.geeksforgeeks.org/network-configuration-trouble-shooting-commands-linux/"><h4>GFG Article</h4></a>

## Difference between http:// and https://

- HTTP uses port number 80 for communication and HTTPS uses 443
- HTTP is considered to be unsecure and HTTPS is secure
- HTTP Works at Application Layer and HTTPS works at Transport Layer
- In HTTP, Encryption is absent and Encryption is present in HTTPS
- HTTP does not require any certificates and HTTPS needs SSL Certificates

To achieve this security in https, Public Key Infrastructure (PKI) is used because public keys can be used by several Web Browsers while private key can be used by the Web Server of that particular website. The distribution of these public keys is done via Certificates which are maintained by the Browser.

## What is an API Gateway?

API is a common software interface that allows two or more applications to communicate. Most apps are built with APIs so it's infrastructure is needed to secure and accelerate the API traffic. Many organisation maintains the APIs but making them secure, traffic handling and all and make the additional revenue.

## What is SSL?

SSL (Secure Sockets Layer) and its successor, TLS (Transport Layer Security), are protocols for establishing authenticated and encrypted links between networked computers. Although the SSL protocol was deprecated with the release of TLS 1.0 in 1999, it is still common to refer to these related technologies as “SSL” or “SSL/TLS.”

An <strong>SSL certificate</strong> (also known as a TLS or SSL/TLS certificate) is a digital document that binds the identity of a website to a cryptographic key pair consisting of a public key and a private key. The public key, included in the certificate, allows a web browser to initiate an encrypted communication session with a web server via the TLS and HTTPS protocols. The private key is kept secure on the server, and is used to digitally sign web pages and other documents (such as images and JavaScript files).

## What’s a proxy server?

A forward proxy, often called a proxy, proxy server, or web proxy, is a server that sits in front of a group of client machines. When those computers make requests to sites and services on the Internet, the proxy server intercepts those requests and then communicates with web servers on behalf of those clients, like a middleman.

For example, let’s name 3 computers involved in a typical forward proxy communication:

- A: This is a user’s home computer
- B: This is a forward proxy server
- C: This is a website’s origin server (where the website data is stored)

<img src="https://www.cloudflare.com/img/learning/cdn/glossary/reverse-proxy/forward-proxy-flow.svg" />

In a standard Internet communication, computer A would reach out directly to computer C, with the client sending requests to the origin server and the origin server responding to the client. When a forward proxy is in place, A will instead send requests to B, which will then forward the request to C. C will then send a response to B, which will forward the response back to A.

Why would anyone add this extra middleman to their Internet activity? There are a few reasons one might want to use a forward proxy:

1. <strong>To avoid state or institutional browsing restrictions</strong> - Some governments, schools, and other organizations use firewalls to give their users access to a limited version of the Internet. A forward proxy can be used to get around these restrictions, as they let the user connect to the proxy rather than directly to the sites they are visiting.
2. <strong>To block access to certain content</strong> - Conversely, proxies can also be set up to block a group of users from accessing certain sites. For example, a school network might be configured to connect to the web through a proxy which enables content filtering rules, refusing to forward responses from Facebook and other social media sites.
3. <strong>To protect their identity online</strong> - In some cases, regular Internet users simply desire increased anonymity online, but in other cases, Internet users live in places where the government can impose serious consequences to political dissidents. Criticizing the government in a web forum or on social media can lead to fines or imprisonment for these users. If one of these dissidents uses a forward proxy to connect to a website where they post politically sensitive comments, the IP address used to post the comments will be harder to trace back to the dissident. Only the IP address of the proxy server will be visible.

## How is a reverse proxy different?

A reverse proxy is a server that sits in front of one or more web servers, intercepting requests from clients. This is different from a forward proxy, where the proxy sits in front of the clients. With a reverse proxy, when clients send requests to the origin server of a website, those requests are intercepted at the network edge by the reverse proxy server. The reverse proxy server will then send requests to and receive responses from the origin server.

The difference between a forward and reverse proxy is subtle but important. A simplified way to sum it up would be to say that a forward proxy sits in front of a client and ensures that no origin server ever communicates directly with that specific client. On the other hand, a reverse proxy sits in front of an origin server and ensures that no client ever communicates directly with that origin server.

Once again, let’s illustrate by naming the computers involved:

- D: Any number of users’ home computers
- E: This is a reverse proxy server
- F: One or more origin servers

<img src="https://www.cloudflare.com/img/learning/cdn/glossary/reverse-proxy/reverse-proxy-flow.svg" />

Typically all requests from D would go directly to F, and F would send responses directly to D. With a reverse proxy, all requests from D will go directly to E, and E will send its requests to and receive responses from F. E will then pass along the appropriate responses to D.

Below we outline some of the benefits of a reverse proxy:

1. <strong>Load balancing</strong> - A popular website that gets millions of users every day may not be able to handle all of its incoming site traffic with a single origin server. Instead, the site can be distributed among a pool of different servers, all handling requests for the same site. In this case, a reverse proxy can provide a load balancing solution which will distribute the incoming traffic evenly among the different servers to prevent any single server from becoming overloaded. In the event that a server fails completely, other servers can step up to handle the traffic.
2. <strong>Protection from attacks</strong> - With a reverse proxy in place, a web site or service never needs to reveal the IP address of their origin server(s). This makes it much harder for attackers to leverage a targeted attack against them, such as a DDoS attack. Instead the attackers will only be able to target the reverse proxy, such as Cloudflare’s CDN, which will have tighter security and more resources to fend off a cyber attack.
3. <strong>Global Server Load Balancing (GSLB)</strong> - In this form of load balancing, a website can be distributed on several servers around the globe and the reverse proxy will send clients to the server that’s geographically closest to them. This decreases the distances that requests and responses need to travel, minimizing load times.
4. <strong>Caching</strong> - A reverse proxy can also cache content, resulting in faster performance. For example, if a user in Paris visits a reverse-proxied website with web servers in Los Angeles, the user might actually connect to a local reverse proxy server in Paris, which will then have to communicate with an origin server in L.A. The proxy server can then cache (or temporarily save) the response data. Subsequent Parisian users who browse the site will then get the locally cached version from the Parisian reverse proxy server, resulting in much faster performance.
5. <strong>SSL encryption</strong> - Encrypting and decrypting SSL (or TLS) communications for each client can be computationally expensive for an origin server. A reverse proxy can be configured to decrypt all incoming requests and encrypt all outgoing responses, freeing up valuable resources on the origin server.

## Load Balancing

Load balancing refers to efficiently distributing incoming network traffic across a group of backend servers, also known as a server farm or server pool.

A load balancer acts as the “traffic cop” sitting in front of your servers and routing client requests across all servers capable of fulfilling those requests in a manner that maximizes speed and capacity utilization and ensures that no one server is overworked, which could degrade performance. If a single server goes down, the load balancer redirects traffic to the remaining online servers. When a new server is added to the server group, the load balancer automatically starts to send requests to it.

In this manner, a load balancer performs the following functions:
- Distributes client requests or network load efficiently across multiple servers
- Ensures high availability and reliability by sending requests only to servers that are online
- Provides the flexibility to add or subtract servers as demand dictates

<img src="https://www.nginx.com/wp-content/uploads/2014/07/what-is-load-balancing-diagram-NGINX-640x324.png" />

##  Address Resolution Protocol

Address Resolution Protocol (ARP) is a communication protocol used to find the MAC (Media Access Control) address of a device from its IP address. This protocol is used when a device wants to communicate with another device on a Local Area Network or Ethernet.

![image](https://user-images.githubusercontent.com/62550592/147722677-cbe70178-913f-4ac0-9f3a-27acac88ea3f.png)

![image](https://user-images.githubusercontent.com/62550592/147722634-62ee9764-d982-4f9f-b14c-27b64b862d16.png)

## Horizontal vs Vertical Scaling

<img src="https://demo.cloudswitches.com/wp-content/uploads/2019/12/redswitches-blog-scaling-image.jpg" />

<hr>

### Horizontal Scaling

Horizontal scaling is a strategy used to enhance the performance of the server node by adding more instances of the server to your existing pool of servers so that the load can be equally distributed.

In horizontal scaling, we do not change the capacity of the individual server, but we decrease the load on the server. Horizontal scalability is achieved with the help of a distributed file system, clustering, and load – balancing.

<strong>Advantages of Horizontal Scaling:</strong>

- Easily scalable tools
- Supporting linear amplifies the capacity
- Easier to run fault-tolerance
- Easy to upgrade
- Better use of smaller systems
- Cost of implementing is less expensive compared to scaling-up

<strong>Disadvantages of Horizontal Scaling:</strong>

- Architectural design is highly complicated
- High licensing fees
- High utility costs such (cooling and electricity)
- Bigger footprint and impact on the data center
- Extra networking equipment such as routers and switches are required

### Vertical Scaling

Vertical Scaling is an attempt to increase the capacity of a single machine. Here the resources such as processing power, storage, memory, and more are added to an existing work unit.

Vertical Scaling is done to increase the capacity of existing hardware or software by adding resources. It can enhance your server without manipulating your code. But it is limited by the fact that you can only get as big as the size of the server.

<strong>Advantages of Vertical Scaling:</strong>

- Reduced software costs.
- Easy Implementation.
- Licensing fees is less.
- Consumes less power.
- Cooling costs are lesser than horizontal scaling.
- Application compatibility is maintained.

<strong>Disadvantages of Vertical Scaling:</strong>

- Limited Scaling.
- The risk for downtime is much higher than horizontal scaling.
- Greater risk of outages and hardware failures.
- Severe vendor lock-in.
- The cost of implementing is expensive.

<hr>

## Caching

Caching is the process of storing copies of files in a cache, or temporary storage location, so that they can be accessed more quickly. Technically, a cache is any temporary storage location for copies of files or data, but the term is often used in reference to Internet technologies. Web browsers cache HTML files, JavaScript, and images in order to load websites more quickly, while DNS servers cache DNS records for faster lookups and CDN servers cache content to reduce latency.

### What does a browser cache do?

Every time a user loads a webpage, their browser has to download quite a lot of data in order to display that webpage. To shorten page load times, browsers cache most of the content that appears on the webpage, saving a copy of the webpage's content on the device’s hard drive. This way, the next time the user loads the page, most of the content is already stored locally and the page will load much more quickly.

Browsers store these files until their time to live (TTL) expires or until the hard drive cache is full. (TTL is an indication of how long content should be cached.) Users can also clear their browser cache if desired.

### What is CDN caching?

A CDN, or content delivery network, caches content (such as images, videos, or webpages) in proxy servers that are located closer to end users than origin servers. (A proxy server is a server that receives requests from clients and passes them along to other servers.) Because the servers are closer to the user making the request, a CDN is able to deliver content more quickly.

<img src="https://www.cloudflare.com/img/learning/cdn/what-is-a-cdn/what-is-a-cdn.png" />

When a user requests content from a website using a CDN, the CDN fetches that content from an origin server, and then saves a copy of the content for future requests. Cached content remains in the CDN cache as long as users continue to request it.

## VIP (Virtual I.P.)

VIP / Virtual IP is that it doesn't correspond to an actual physical network interface or port. The purpose of VIP is to provide IP addresses that can float between two or more physical network nodes and provide redundency.

Used in First Hop redundancy protocols ( like HSRP, GLBP, VRRP) to represent the IP as gateway for end Hosts but actually not configured on any interface rather it is shared by all devices in the configured protocol.

Used in applications , where an application hosted in server has an IP address on a physical subnet and application has configured with different IP.

In Load Balancers VIP's are mapped with multiple Physical host IP address ... All traffic directed to VIP and Load balancer will distribute traffic to servers based on Load balancing algorithm configured.

## REST API vs HTTP API

REST refers to a set of attributes of a particular architectural style, while HTTP is a well-defined protocol that happens to exhibit many features of a RESTful system.

<a href="https://www.baeldung.com/cs/rest-vs-http">Read More</a>

## Container in Computer Networks

Container Networking is an emerging application sandboxing mechanism used in home desktops and web-scale enterprise networking solutions similar in concept to a virtual machine. Isolated inside the container from the host and all other containers are a full-featured Linux environment with its own users, file system, processes, and network stack. All applications inside the container are permitted to access or modify files or resources available inside the container only.

It is possible to run multiple containers at the same time, each with their own installations and dependencies. This is particularly useful in instances when newer versions of an application may require a dependency upgraded that may cause conflicts with other application dependencies running on the server. Unlike virtual machines, containers share host resources rather than fully simulating all hardware on the computer, making containers smaller and faster than virtual machines and reducing overhead.

## Containerization or virtualization

Virtualization enables you to run multiple operating systems on the hardware of a single physical server, while containerization enables you to deploy multiple applications using the same operating system on a single virtual machine or server. 

## Performance vs. Scalability

Performance refers to the capability of a system to provide a certain response time. server a defined number of users or process a certain amount of data.

Scalability referes to the characteristic of a system to increase performance by adding additional ressources (servers).

## Latency vs Throughput

Latency indicates how long it takes for packets to reach their destination. Throughput is the term given to the number of packets that are processed within a specific period of time.

## VPN (Virtual Private Network)

VPNs encrypt your internet traffic and disguise your online identity. This makes it more difficult for third parties to track your activities online and steal data. The encryption takes place in real time.

### How does a VPN work?

A VPN hides your IP address by letting the network redirect it through a specially configured remote server run by a VPN host. This means that if you surf online with a VPN, the VPN server becomes the source of your data. This means your Internet Service Provider (ISP) and other third parties cannot see which websites you visit or what data you send and receive online. A VPN works like a filter that turns all your data into "gibberish". Even if someone were to get their hands on your data, it would be useless.

<a href="https://www.kaspersky.com/resource-center/definitions/what-is-a-vpn">Read More</a>

## Router vs Gateway

### Router

A router is basically a device or a hardware which is responsible for receiving, analyzing and forwarding the data packets to other networks. A router actually determines the destination or the target IP address of the packet and thus the best way for transferring the packet is determined by the help of forwarding tables and headers. The forwarding of the data packet is done from one router to the other which basically forms a network(example: internet) until it reaches the final target node.

### Gateway

A gateway is basically a device or a hardware which acts like a “gate” among the networks.Thus it can also be defined as a node which acts as an entrance for the other nodes in the network.It is also responsible for enabling the traffic flow within the network.Gateway uses more than one protocol for communication thus its activities are much more complex than a switch or a router. So a gateway is basically a device that is used for the communication among the networks which have a different set of protocols and is responsible for the conversion of one protocol into the other.

## NIC amd MAC Address

A NIC is a special hardware card within any networked device (computer, printer, router, etc.) that handles all the technical aspects of sending and receiving data packets over a computer network.

Like your mailing address at home, your computer's NIC has a unique address. This address must be unique, otherwise, network traffic cannot find its way to the right computer.

The distinctive address that identifies a NIC is called the Media Access Control (MAC) address. A MAC address is formatted as a six-byte, hexadecimal number

```
00:90:7F:12:DE:7F
```

### Why do we need IP when we have MAC?

Actually MAC address are fixed hence they are not as scalable compared to IP address. IP address have several other features like subnetting and supernetting which gives a logical understanding of the presence of a machine in a network. These facilities are not with the MAC address.

Also MAC address are not routable. The Internet Protocols will not treat them as an address of a source or destination. Hence IP address in many ways simplifies our task.

## Private and Public IP addresses

<strong>Private IP address</strong> of a system is the IP address which is used to communicate within the same network. Using private IP data or information can be sent or received within the same network.

<strong>Public IP address</strong> of a system is the IP address which is used to communicate outside the network. Public IP address is basically assigned by the ISP (Internet Service Provider).

## What is Multiplexing?

Multiplexing is a technique used to combine and send the multiple data streams over a single medium. The process of combining the data streams is known as multiplexing and hardware used for multiplexing is known as a multiplexer.

Multiplexing is achieved by using a device called Multiplexer (MUX) that combines n input lines to generate a single output line. Multiplexing follows many-to-one, i.e., n input lines and one output line.

Demultiplexing is achieved by using a device called Demultiplexer (DEMUX) available at the receiving end. DEMUX separates a signal into its component signals (one input and n outputs). Therefore, we can say that demultiplexing follows the one-to-many approach.

## Modem vs Router

### Modem

A modem is a device that modulates or demodulates the signal. It maintains a dedicated connection with the ISP to get the internet connection for home or business.

Modem connects between your computer/router and your ISP/cloud and converts the digital signal from your computer/router to analog and vice versa

### Router

The router is a networking device responsible for routing the data packets from source to destination over a network. It distributes or routes the internet connection from the modem to all the networking devices, either wired or wireless, such as PC, Laptop, Mobile phone, tablet, etc. It also enables multiple devices to communicate with each other over the same network.

## How Bluetooth works

Bluetooth enabled electronic devices connect and communicate wirelessly through shortrange devices known as Piconets. Bluetooth devices exist in small ad-hoc configurations with the ability to act either as master or slave the specification allows a mechanism for master and slave to switch their roles. Point to point configuration with one master and one slave is the simplest configuration.

When more than two Bluetooth devices communicate with one another, this is called a PICONET. A Piconet can contain up to seven slaves clustered around a single master. The device that initializes establishment of the Piconet becomes the master.

The master is responsible for transmission control by dividing the network into a series of time slots amongst the network members, as a part of time division multiplexing scheme which is shown below.

<img src="https://www.tutorialspoint.com/wireless_communication/images/piconet.jpg" />

## How Hotspot works


