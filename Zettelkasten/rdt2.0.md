Created on: 13-08-2024 16:06
Status: #idea
Tags: #networks 
# rdt2.0
__channel with bit errors__
- *Receiver:* checks checksum
	- If not corrupted, sends ACK, extracts data and delivers data to application layer
	- If corrupted, sends NAK and throws away message. 
- *Sender:* sends package and waits for positive (ACK) or negative (NAK) acknowledgement message
- how to recover from bit flip errors?
	 co-operation between sender and receiver, sender asks receiver to send message again when it detects an error.
#### Flaw in rdt2.0:
 > if ACK/NAK is corrupted, sender will send same message again. This will create duplicates at receiver
 
 ![[rdt2.0.gif]]



-----------------
# References
[[Computer Networks]]