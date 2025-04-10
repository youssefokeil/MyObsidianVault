Created on: 17-08-2024 14:40
Status: #idea
Tags: #networks 
# Go-back-N
> - Receiver uses cumulative ack: meaning the receiver doesn't acknowledge packet if packet before it was not acknowledged.
> - Sender retransmits all unacked packets, starting from the oldest unacked packet.


### How it works?
- Sender has a sliding window of N packets, as acknowledgement of one packet is received from receiver, the sender slides its window
- If receiver doesn't send ACK for a specific packet , all consecutive packets won't send an ACK message and receiver won't accept them.
- Sender waits for timeout and retransmits entire window

### Pros and Cons:
- Simple
- Inefficient for noisy links

![Go Back N demonstration (youtube.com)](https://www.youtube.com/watch?v=gaocB7unrqs)



-----------------
# References
[[Computer Networks]]