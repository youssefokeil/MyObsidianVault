Created on: 13-08-2024 17:18
Status: #idea
Tags: #networks 
# rdt3.0
assumes underlying channel can lose packets. 
	Ex: ACK not transmitted to sender:
	- Sender then guesses whether message is dropped or the ACK itself?

**Fix:**
	Waiting a reasonable amount of time for ACK, retransmit when ACK not sent in that time.
	- if messages is queued not lost, the receiver will get a duplicate but it'll know from the seq #.
	- requires countdown timer

FSM is similar to rdt2.2, with extra timeout loop.
![[rdt3_sender.png]]

### Timeout:
In this we use stop-and-wait operation.:
> choosing the correct timeout is challenging, because usually we have transmission delay << Round trip time. This leads to low utilization in the network. To fix this we use [[Pipelining (Networks)]]


----------------- 
# References
[[Computer Networks]]