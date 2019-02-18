# Protocol layering [contd...]

### Application Layer

Here network applications and their application-layer protocols reside. 

Ex:
- HTTP protocol (which provides for Web document request and transfer)
- SMTP (which provides for the transfer of e-mail messages)
- FTP (which provides for the transfer of files between two end systems)

An application-layer protocol is distributed over multiple end systems, with the application in one end system using the protocol to exchange packets of information with application in another end system. We'll refer to this packet of information at the application layer as a message. 

### Transport Layer

The Internet's transport layer transports application-layer messages between application endpoints. In the Internet ther are two transport protocols, TCP and UDP, either of which can transport application-layer messages. 

- TCP provides a connection-oriented service to its apps
- guaranteed delivery of application-layer messages to the destination
- flow control (sender/receiver speed matching)
- breaks long messages into shorter segments and provies a congestion-control mechanism, so that a source throttles its transmission rate when the network is congested. 

- UDP protocol provides a connectionless service to its applications.
- no reliability, no flow control, and no congestion control

We'll refer to a transport-layer packet as a **segment**.

### Network Layer

Responsible for moving network-layer packets known as **datagrams** from one host to another.

:point_right: Transport layer protocol in a source host passes a transport-layer segment and a destination address to the network layer which then provides the service of delivering the segment to the transport layer in the destination host.

:point_right: The network layer includes the **IP protocol**, which defines the fields in the datagram as well as how the end systems and routers act on these fields. 

> Thers is only one IP protocol, and all Internet components that have a network layer must run the IP protocol. The Internet's network layer also contains routing protocols that determines the routers that datagrams take between sources and destinations. 
> The Internet has many routing protocols. 
> Within a network, the network administrator can run any routing protocol desired. 

### Link layer

At each node, the network layer passes the datagram down to the link layer, which delivers the datagram to the next node along the route. At this next node, the link layer passes the datagram up to the network layer. 

> The services provided by the link layer depend on the specific link-layer protocol that is employed over the link 

Ex: Ethernet, WiFi, and the cable access network's DOCSIS protocol.

:point_right: As datagrams typically need to traverse several links to travel from source to destination, a datagram may be handled by different link-layer protocols at different links along its route. Ex: Ethernet on one link and PPP on next

The network layer will receive a different service from each of the different link-layer protocols. We'll refer to the link-layer packets as **frames**

### Physical Layer 

While the job of the link layer is to move entire frames from one network element to an adjacent network element, the job of the physical layer is to move the individual bits within the frame from one node to the next. 

The protocols in this layer are again link dependent and further depend on the actual transmission medium of the link.

### The OSI Model 

**Open Systems Interconnection**

seven layers: 
1. Application layer
2. Presentation layer
3. Session layer
4. Transport layer
5. Network layer
6. data link layer
7. Physical layer

#### Presentation layer

provides services that allow communicating applications to interpret the meaning of data exchanged. These services include data compression and data encryption as wll as dat description t (regarding formats of file). 

#### Session layer

provides for delimiting and synchronization of data exchange, including the means to build a checkpointing and recovery scheme

> In the today's Internet these two layers come under application layer i.e it's up to the application developer to build that functionality into the application.

 

