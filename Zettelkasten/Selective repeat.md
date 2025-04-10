Created on: 17-08-2024 15:05
Status: #idea
Tags: #networks 
# Selective repeat
> Sender only resends the specific packet that was lost.
> The sender and receiver both have large windows and the retransmission is only on one packet in the window.

### How it works?
- Sender sends packets
- One of the packets is killed
- Either the receiver sends NACK for the specific packet that was killed after receiving a packet that is next in queue. 
	- Ex: Receiver receives packet 4 and packet 3 was not retransmitted yet. Receiver sends NACK3
- Or the sender waits for the timeout of the acknowledgement of the packet and resends when it finds that the timeout is passed

### Pros and Cons:
- Complicated
- Suitable for noisy links.

![Selective retransmission demonstration (youtube.com)](https://www.youtube.com/watch?v=6fz_Wo8jkAc)


-----------------
# References
[[Computer Networks]]