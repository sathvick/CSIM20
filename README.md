# CSIM20

Design and develop a simple inter-process communication protocol that fulfills the following
requirements. Refer to the example code shown in the lecture note #3.
• There are five nodes in a network and each node is fully connected with others. Each node
generates a HELLO packet with the inter arrival time following the exponential distribution
(average 5 seconds).
• A sender transmits a HELLO packet to a randomly chosen receiver. Upon receiving, the receiver
replies a HELLO_ACK packet back. If the sender receives the HELLO_ACK, then the
transmission is successful. Suppose it takes 0.1 seconds to transmit the packet over the network
(e.g., transmission time). The transmission delay (e.g., local processing time) is 0.2.
• Due to the unreliable link quality, packets can be lost and there is a set of packet loss
probabilities (0.1, 0.2, 0.3, 0.4, or 0.5). If the sender does not receive the HELLO_ACK packet
within a timeout period (2 seconds), it retransmits a HELLO packet. If the sender still does not
receive the HELLO_ACK, then the transmission is failed.
• Dump a snapshot of events (i.e., the packet loss probability = 0.3). Only one-page would be
enough. For example,
...
node.0 sends a HELLO to node.3 at 100.2 seconds.
node.2 replies a HELLO_ACK to node.1 at 100.4 seconds
node.4 sends a HELLO to node.3 at 110.5 seconds
node.1 receives a HELLO_ACK from node.2 at 110.6 seconds
node.4 re-sends a HELLO to node.3 at 111.5 seconds
...
• The simulation ends when the simulation time reaches 1000.
• Draw result graphs showing the following performance metrics against the packet loss
probabilities (0.1, 0.2, 0.3, 0.4, or 0.5).
Average number of successful transmissions
Average number of failed transmissions
Average roundtrip time 
