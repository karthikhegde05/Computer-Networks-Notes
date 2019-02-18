# Throughput in Computer Networks

Consider transfering a large file from Host A to Host B across a computer network. The **instantaneous throughput** at any instant of time is the rate (in bits/sec) at which Host B is receiving the file. 

If the file consists of F bits and the transfer takes T seconds for Host B to receive all F bits, then the **average throughput** of the file transfer is F/T bis/sec. 

- For a simple two-link network, the throughput is min{R<sub>c</sub>, R<sub>s</sub>}, i.e, it is the transmission rate of the bottleneck link.

- For a network with N links between the server and the client, with the transmission rates of the N links being R<sub>1</sub>, R<sub>2</sub>, ..., R<sub>N</sub> throughput is min{R<sub>1</sub>, R<sub>2</sub>, ..., R<sub>N</sub>} which is once again the transmission rate of the bottleneck link along the path between server and client.

Consider the throughput for a file transfer from the server to the client in today's Internet. The server is connected to the network with an access link of rate R<sub>s</sub> and the client is connected to the network with an access link of rate R<sub>c</sub>. Now suppose that all the links in the core of the communication network have very high transmission rates then throughput = min{R<sub>s</sub>, R<sub>c</sub>}. Therefore the constraining factor for throughput in today's Internet is typically the access network.

# Protocol Layers and Their Service Models

### Layered Architecture

A layered architecture allows us to discuss a well-defined, specific part of a large and complex system. This simplification itself is of considerable value by providing modularity, making it easier to change the implementation of the service provided by the layer. 

### Protocol Layering 

To provide structure to the design of network protocols, network designers organize protcols in layers. Each protocol belongs to one of the layers. 

We are interested in the services that a layer offers to the layer above - the so-called service model of a layer. 

Each layer provides its service by:

1. performing certain actions within that layer and 
2. by using the services of the layer directly below it. 

The  Five-layer Internet Protocol stack
1. Application
2. Transport
3. Network 
4. Link
5. Physical 

:point_right: Application layer protocols such as HTTP and SMTP are almost always implemented in software in the end systems; so are transport-layer protocols. 

:point_right: Because the physical layer and data link layers are responsible for handling communication over a spcific link, they are typically implemented in a network interface card(ex: Ethernet/ WiFi interface cards) associated with a given link. 

:point_right: The network layer is often a mixed implementation of hardware and software. 

:point_right: the layered protocol is distributed among the end systems, packet switches, and other components that make up the network. That is, there's often a piece of a layer n protocol in each of these network components. 

#### Drawbacks of layering

One layer may duplicate lower-layer functionality. Ex: Many protocol stacks provide error recovery on both a per-link basis and an end-to-end basis. 

Functionality at one layer may need information(ex: a time-stamp value) i.e present only in another layer
