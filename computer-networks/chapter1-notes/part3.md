# Delay, Loss and Throughput in Packet-Switched Networks

### Delay 

- nodal processing delay
- queuing delay
- transmission delay
- propagation delay

together :point_right: give a **total nodal delay**

### Processing Delay

the time required to examine the packet's header and determine where to direct the packet 

> the processing delay can also include other factors, such as teh time needed to check for bit-level errors in the packet that occured in transmitting the packet's bits. 

### Queuing Delay

the packet experiences a queuing delay as it waits to be transmitted onto the link. 

- The length of the queuing delay of a specific packet will depend on the traffic

### Transmission Delay

Assuming that packets are transmitted in a FIFO, the packet can be transmitted only after all the packets that have arrived before it have been transmitted. 

the length of the packet is L bits, the transmission rate of the link from router A to router Bis R bits/sec. Then the transmission delay is L/R.

### Propagation Delay

The time required to propagate from the beginning of the link to router B is the propagation delay.

The bit propagated at the propagation speed of the link. (<= speed of light). The propagation speed depends on the physical medium of the link. 

The propagation delay is the distance between two routers divided by the propagation speed.  

d<sub>nodal</sub> = d<sub>proc</sub> + d<sub>queue</sub> + d<sub>trans</sub> + d<sub>prop</sub>

> The contribution of these delay components can vary significantly. d<sub>proc</sub> can be negligible for a link within the same university campus; d<sub>prop</sub> can be the dominant term; d<sub>trans</sub> can range from negligible to significant. The processing delay is often negligible. However, it strongly influences a router's maximum throughput, which is the maximum rate at which a router can forward packets.  
