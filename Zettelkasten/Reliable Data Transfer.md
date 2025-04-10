Created on: 13-08-2024 15:05
Status: #idea
Tags: #networks 
# Reliable Data Transfer
Lots of protocols are under the reliable data transfer umbrella:
- [[rdt1.0]]: assumes no bit errors/losses
- [[rdt2.0]]: 
	- adds checksum message and ACK/NAK message from receiver is based on that checksum.
	-  Assumes ACK/NAK isn't corrupted, which can create duplicates at receiver
- [[rdt2.1]]:
	 - Builds on rdt2.0 by adding checksums and ACK/NAK  messages
	 - adds seq no. to messages, and in turn to the ACK/NAK messages,  to combat the duplicate issue
- [[rdt2.2]]: 
	- Simplifies things by ditching the NAK message, replacing it with ACK with the wrong seq. no.
- [[rdt3.0]]:
	- assumes underlying channel can lose packets and adds a timeout, to see if message is lost or just queued
	- if ACK doesn't return in that timeout period, resends packet
	- Only uses positive acknowledgements like rdt2.2





-----------------
# References
[[Computer Networks]]