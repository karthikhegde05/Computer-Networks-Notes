## The Network Core

### Packet Switching

- In a network application, end systems exchange messages with each other. To send a message a from a source end system to a destinatio end system, the source breaks long messages into smaller chunks of data known as packets.

- Between source and destination, each packet travels through communication links and packet switches

- Packets are transmitted over each communication link at a rate equal to full transmission rate of the link. So, if a source end system or a packet switch is sending a packet of L bits over a link with transmission rate R bits/sec, then the time to transmit the packet is L/R seconds.

#### Store-and-Forward Transmission

- The packet switch must receive the entire packet before it can begin to transmit the first bit of the packet onto the outbound link. 

- This means that a router connected between two end systems(router will have many links) and whose job is to switch an incoming packet onto an outgoing link will store the incoming packet's bits. Only after the router has received all of the packet's bits it begins to forward the packet onto the outbound link.

- The general case of sending one packet from source to destination over a path consisting of N links each of rate R(N-1 routers) 
>	d<sub>end-to-end</sub> = NL/R

#### Queuing Delays and Packet loss

Each packet switch has multiple links attached to it. For each attached link, the packet switch has an output buffer(output queue), which stores packets that the router is about to send into that link. 

> If an arriving packet needs to be transmitted onto a link but finds the link busy with the transmission of another packet, the arriving packet must wait in the output buffer. Thus in addition to **store-and-forward** delays, packets suffer output buffer queuing delays. 

- Queuing delays depend on the level of congestion in the network. 

> Since the amount of buffer space is finite, an arriving packet may find that the buffer is completely full with other packets waiting for transmission. In this case, **packet loss** will occur - either the arriving packet or one of the already queued packets will be dropped.

#### Forwarding Tables and Routing Protocols

A router takes a packet arriving on one of its attached communication links and forwards that packet onto another one of its attached communication links. But how does the router determine which link it should forward the packet onto? 

> Packet forwarding is actually done in different ways in different types of computer networks.

- In the Internet, every end system has an address called an IP address. When a source end system wants to send a packet to a destination end system, the source includes the destination's IP address in the packet's header. 

- When the packet arrives at a router in the network, the router examines a portion of the packet's destination address and forwards the packet to an adjacent router. Each router has a **forwarding table** that maps destination addresses (or portions of the destination addresses) to that router's outbound links. When a packet arrives at a router, the router examines the address and searches its forwarding table, using this destination address, to find the appropriate outbound link.

> Now how do **forwarding tables** get set?

>Ans: the Internet has a no. of special **routing protocols** that are used to automatically set the forwarding tables. A routing protocol may, for example, determine the shortest path from each router to each destination and use the shortest path results to configure the forwarding tables in the routers.

### Circuit Switching 

Like packet switching **circuit switching** is another way to move data through a network of links and switches.

In this kind of networks, the resources needed along apath(buffers, link, transmission rate) to provide for communication between end systems are reserved for the duration of the communication session between the end systems. This was not the case in packet switching - the resources are not reserved. a session's messages use the resources on demand, and as a consequence, may have to wait (queue) for access to a communication link

> Example is Traditional telephone networks

> when the network establishes the circuit, it also reserves a constant transmission rate in the networks's links (representing a fraction of link's total transmission capacity) for the duration of the connection.  

> Since a given transmission rate has been reserved for this sender-to-receiver connection, the sender can transfer the data to the receiver at the *guaranteed* constant rate. 

#### Multiplexing in Circuit-Switched Networks

A circuit in a link is implemented with either **frequency-division multiplexing (FDM) or time-division multiplexing (TDM)

- With FDM, the frequency spectrum of a link is divided up among the connections established across the link. The link dedicates a frequency band to each connection for the duration of the connection. 
> Ex: Telephone networks and FM radio stations use FDM

- For TDM link, time is divided into frames of fixed duration, and each frame is divided into a fixed number of time slots. When the network establishes a connection across a link, the network dedicates one time slot in every frame to this connection. These slots are dedicated for the sole use of that connection, with one time slot available for use (in every frame) to transmit the connection's data. 

> For TDM, the transmission rate of a circuit is equal to the frame rate multiplied by the number of bits in a slot. Ex: if the link transmits 8000 frames per sec and each slot consists of 8 bits, then the transmission rate of a circuit is 64 kbps.

> Proponents of packet switching have always argued that circuit switching is wasteful because the dedicated circuits are idle during **silent periods**.

#### Packet Switching Vs Circuit Switching

> Critics of packet switching have often argued that packet switching is not suitable for real-time services (telephone calls, video conference calls) whereas the proponents of packet switching argue that it offers better sharing of transmission capacity than circuit switching and that it is simpler, more efficient, and less costly to implement than circuit switching.

>Why is packet switching more efficient?

- Circuit Switching pre-allocates use of the transmission link regardless of demand, with allocated but unneeded link time going unused. Packet switching on the other hand allocated link use on demand. Link transmission capacity will be shard on a packet-by-packet basis only among those users who have packets that need to be transmitted over the link. 

> Although both forms are prevalent in today's telecommunication networks, the trend has certainly been in the direction of packet switching.  
