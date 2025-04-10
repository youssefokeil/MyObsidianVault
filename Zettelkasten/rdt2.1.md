Created on: 13-08-2024 16:07
Status: #idea
Tags: #networks 
# rdt2.1
fixes duplicate error in [[rdt2.0]], by adding bit that is responsible for sequence number. This bit switches from 0 to 1.
- *Sender:*
	- Checks ACK/NAK corrupted
	- Must remember expected pkt sequence no. should be 0 or 1
- *Receiver:*
	 - Checks if received pkt is duplicate, by checking if seq. number is repeated 

![[rdt2.1.png]]

-----------------
# References
[[Computer Networks]]