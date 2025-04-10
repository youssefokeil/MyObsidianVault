Created on: 17-08-2024 22:39
Status: #idea
Tags: #networks
# Congestion Control
> A mechanism that controls the entry of data packets into the network. Avoiding congestion in underlying infrastructure.

### Detection:
Congestion control usually use end-to-end notification, by waiting for receiver to send ACKs or for sender to reach timeout.
- lost packets, meaning overflow at buffers
- long delays, long queues in router buffers
There's also a new implementation that is not so used, called [[Explicit Congestion Notification (ECN)]], that doesn't use end-to-end notification.

### Solutions:
Increase transmission rate until you find
- lots of duplicates
- lots of timeouts
#### Approach:
__

-----------------
# References
[[Computer Networks]]