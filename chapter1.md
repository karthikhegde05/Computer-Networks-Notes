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

- Asymmetric :point_right: downstream rate (42.8Mbps) > upstream rate (30.7 Mbps)

- it is shared broadcast medium :point_right: every packet sent by the head end travels downstream on every link to every home and every packet sent by a home travels on the upstream channel to the head end.

- Because the upstream channel is also shared, a distributed multiple access protocol is needed to coordinate transmissions and avoid collisions.

#### FTTH

fiber to the home(FTTH) - provides an optical fiber path from the CO directly to the home. 

> the simplest optical distribution network is called direct fiber, with one fiber leaving the CO for each home. More commonly, each fiber leaving the CO is actually shared by many homes; it is not until the fiber gets relatively close to the homes that it is split into individual customer-specific fibers. There are two competing optical-distribution network architectures that perform this splitting: 
> 1. active optical networks(AONs) :point_right: essentially switched Ethernet
> 2. passive optical networks(PONs)

##### FTTH using PON

> extension of previous section

- Each home has an optical network terminator(ONT), which is connected by dedicated optical fiber to a neighborhood splitter.

- the splitter combines a no. of homes onto a single, shared optical fiber, which connects to an optical line terminator(OLT) in the telco's CO.

- the OLT, providing conversion between optical and electrical signals, connects to the Internet via a telco router. In the home, users connect a home router(typically a wireless router) to the ONT and access the Internet via this home router. 

- In the PON architecture, all packets sent from OLT to the splitter are replicated at the splitter(similar to a cable head end)

> FTTH can provide Internet access rates in the gigabits per second range.

> :point_right: :point_right: 2 other access network technologies are also used to provide Internet access to the home they are :point_right: Satellite link and Dial-up access(based on sme model as DSL) and these are very slow

### Access in the Enterprise(and the Home): Ethernet and WiFi

On a corporate level, a local area network(LAN) is used to connect an end system to the edge router. Although there are many types of LAN technologies, Ethernet is by far the most prevalent access technology in corporate networks.

- Ethernet users use twisted-pair copper wire to connect to an Ethernet switch. The Ethernet switch, or a network of such interconnected switches, is then in turn connected into the larger Internet.

> With Ethernet access, users typically have 100 Mbps access to the Ethernet switch, whereas servers may have 1 Gbps/ 10 Gbps

- In a wireless LAN setting, wireless users transmit/receive packets to/from an access point that is connected into the enterprise's network(most likely including wired Ethernet), which in turn is connected to the wired Internet. 

- A wireless LAN user(a.k.a WiFi) is now everywhere.

> Ethernet and WiFi have recently become common in the components of home networks. Many homes combine broadband residential access(cable modems/DSL) with these inexpensive wireless LAN technologies to create powerful home networks. 
   
### Wide-Area Wireless Access: 3G and LTE

devices like iPhones, Blackberrys and Android devices employ the same wireless infrastructure used for cellular telephony to send/receive packets through a base station that is operated by the cellular network provider. Unlike WiFi, a user need only be within a few tens of kilometers(as opposed to a few tens of meters) of the base station.

> Telecom companies have mad enormous investments in so-called third-generation(3G) wireless, which provides packet-switched wide-area wireless Internet access at speeds in excess of 1 Mbps. But even higher-speed wide-area access technologies-a fourth generation(4G) of wide-area wireless networks-are already being deployed. LTE (Long Term Evolution) has its roots in 3G technology, and can potentially achieve rates in excess of 10 Mbps.

### Physical media 

Goto this link :point_right: [Phyiscal Media](https://www.geeksforgeeks.org/types-transmission-media/)
