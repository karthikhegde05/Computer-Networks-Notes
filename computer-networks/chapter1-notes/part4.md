# Queuing Delay and Packet Loss

The most complicated and interesting component of **nodal delay** is the queuing delay d<sub>queue</sub>

Unlike the other three delay, the queuing delay can vary from packet to packet. Expressed as average queuing delay, variance of queuing delay and the probability that the queuing delay exceeds some specified value.

> When is the queuing delay large and when is it insignificant?

It depends on the rate at which traffic arrives at the queue, the transmission rate of the link, & the nature of the arriving traffic.

:point_right: let a -> average rate at which packets arrive at the queue(packets/sec); R->transmission rate(bits/sec); for simplicity, let all packets consist of L bits. 

Then the average rate at which bits arrive at the queue is La bits/sec. Assuming that queue is very big, so that it can hold essentially an infinite number of bits. The ratio La/R (a.k.a **traffic intensity**) plays an important role in estimating the extent of the queuing delay. 

> If La/R > 1, then the average rate at which bits arrive at the queue exceeds the rate at which the bits can transmitted from the queue. In this unfortunate situation, the queue will tend to increase without bound and the queuing delay will approach infinity!

### Packet Loss

In reality a queue preceding a link has finite capacity, although the queuing capacity greatly depends on the router design and cost. 

:point_right: As this is the case, packet delays do not really approach infinityas the traffic intensity approaches 1. Instead, a packet can arrive to find a full queue. With no place to store such a packet, a router will drop that packet. 

:point_right: The fraction of lost packets increases as the traffic intensity increases. Thus performance at a node is often measured not only in terms of delay, but also in terms of the probability of packet loss. A lost packet may be retransmitted on an end-to-end basis in order to ensure that all data are eventually transferred from source to destination.

### End-to-End Delay

Our discussion up to this point has focused on the nodal delay, i.e, the delay at a single router. Let's now consider the total delay fom source to destination.

Suppose there are N-1 routers in this path, and also that the network is uncongested (so queuing delays are negligible) then

d<sub>end-end</sub> = N(d<sub>proc</sub> + d<sub>trans</sub> + d<sub>prop</sub>)

### Traceroute

read the textbook

### End System, Application, and Other Delays

In addition to processing, transmission, and propagation delays, there can be additional significant delays in the end systems.

Ex: an end system wanting to transmit a packet into a shared medium(WiFi, or cable modem scenario) may purposefully delay its transmission as part of its protocol for sharing the medium with other end systems.

> Another important delay is media packetization delay, which is present in Voice-over-IP(VoIP) applications. In VoIP, the sending side must first fill a packet with encoded digitized speech before passing the packet to the Internet. This time to fill a packet - called the packetization delay - can be significant and can impact the user-perceived quality of a VoIP call. 
