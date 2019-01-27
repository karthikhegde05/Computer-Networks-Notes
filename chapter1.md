# COMPUTER NETWORKS AND INTERNET

>This section does not contain everything from the book

### Network Protocols

A protocol defines the format and order of messages exhanged between two or more communicating entities, as well as the actions taken on the  transmission and/or receipt of a message or other event.

>Mastering the field of computer networking is equivalent to understanding the what, why, and how of networking protocols.

### The Network Edge

The computers and other devices connected to the internet are end-system(a.k.a hosts)

Ex:
 >desktop computers, servers.

hosts are divided into two categories:
>clients
>servers

### Access Networks

Access network is the network that physically connects an end system to the first router(a.k.a "edge router") on a path from the end system to any othe distant end system.

### Home Access:DSL, Cable, FTTH, Dial-Up, and Satellite

Two most prevalent types of broadband residential access:

1. Digital Subscriber Line(DSL)

2. Cable

#### DSL

A residence obtains DSL Internet access from the same local telephne company(telco) that provides its wired local phone access. Thus, when DSL is used, a customer's telco is also its ISP. 

- the DSL modem exchanges digital data with a digital subscriber line access multiplexer(DSLAM) located in telco's local CO

- The home's DSL modem takes digital data and translates it to high-frequency tones for transmission over telephone wires to the CO(telco's central office)

- the analog signals from many such homes are translated back into digital format at the DSLAM

>The residential telephone line carries both data and traditional telephone signals simultaneously, which are encoded at different frequencies:
> 1. A high-speed downstream channel (50 kHz to 1MHz band) 
> 2. A medium-speed upstream channel (4kHz to 50kHz band)
> 3. An ordinary two-way telephone channel (0 to 4kHz band)

> This makes DSL link and telephone connection separate. This technique is called Frequency Division Multiplexing

Here the downstream(12Mbps) and upstream(1.8Mbps) transmissio rates are different :point_right: Asymmetric.

>Engineers have expressly designed DSL for short distances between the home and the CO.

#### Cable

Here local cable television company acts as an ISP. Cable Internet access makes use of the television company's existiing cable television infrastructure

- fibre optics connect the cable head end to neighborhood-level junctions, from which traditional coaxial cable is then used to reach individual houses and apartments. Due to use of both fibre and coaxial cable this system is often referred to as Hybrid Fiber Coax(HFC)

- Cable modems is typically an external device and connects to the home PC through an Ethernet port.

- At the cable head end, the cable modem termination system(CMTS) serves a similar function as the DSL network's DSLAM(turning the analog signal sent from the cable modems in many downstream homes back into digital format)

- Asymmetric :pont_right: downstream rate (42.8Mbps) > upstream rate (30.7 Mbps)

- it is shared broadcast medium :point_right: every packet sent by the head end travels downstream on every link to every home and every packet sent by a home travels on the upstream channel to the head end.

- Because the upstream channel is also shared, a distributed multiple access protocol is needed to coordinate transmissions and avoid collisions.

#### FTTH

fiber to the home(FTTH) - provides an optical fiber path from the CO directly to the home. 

> the simplest optical distribution network is called direct fiber, with one fiber leaving the CO for each home. More commonly, each fiber leaving the CO is actually shared by many homes; it is not until the fiber gets relatively close to the homes that it is split into individual customer-specific fibers. There are two competing optical-distribution network architectures that perform this splitting: 
> 1. active optical networks(AONs) :point_right: essentially switched Ethernet
> 2. passive optical networks(PONs)

-  
