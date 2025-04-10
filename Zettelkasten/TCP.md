Created on: 13-08-2024 13:33
Status: #idea
Tags: #networks
# TCP Transmission Control Protocol
> Is a [[transport layer]] protocol that is connection-oriented, meaning that sender and receiver must establish a connection first before sending and receiving data. Usually the setup is using a handshake.

__Services Provided:
- Congestion control
- Flow control
- Connection setup, using handshakes 
- Reliable data transfer
- In - order data transfer

If application doesn't need reliable data service they can use [[UDP]]

### TCP segment structure:
![[img002.gif]]
- Sequence number: has the number of first byte in segment's data
- Acknowledgement number: number of first byte in next segment


-----------------
# References
[[Computer Networks]]