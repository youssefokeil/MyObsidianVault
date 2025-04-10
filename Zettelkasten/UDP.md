Created on: 13-08-2024 13:38
Status: #idea
Tags: #networks
# UDP User Datagram protocol
> is a [[transport layer]] protocol that is connectionless. Meaning the sender and receiver don't need to negotiate a connection before sending data. {RFC 768 }

###  Features:
- Best-effort service, UDP segments may:
	1. lost
	2. delivered out-of-order to app
	try to let your messages self-contained and have no relationship with previous or upcoming messages.
- faster than TCP
- Simple and stateless
- Connectionless
	1. No handshaking between sender and receiver
	2. Each UDP segment handled independently

__Used for:__
- Transaction-oriented simple query responses such as [[DNS]]
- Streaming media because it's loss tolerant

__To make it reliable:__
- add reliability at application layer

### Segment Structure:

![[091-udp-user-datagram-protocol-01.png]]
- Small header size
- Uses [[checksum]]
- The UDP header length field is the length of the UDP header plus the UDP data
-----------------
# References
[[Computer Networks]]