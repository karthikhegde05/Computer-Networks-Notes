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

 
