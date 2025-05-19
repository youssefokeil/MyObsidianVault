Created on: 07-05-2025 06:30
Status: #idea
Tags: #distributed_systems #data_base
# Navigation in Name Services
>Act of chaining multiple name services, in order to resolve a single name

### Iterative Navigation
- a client iteratively contacts name services to resolve a name
- used in [[DNS]] as the standard
![[Screenshot From 2025-05-07 06-33-19.png|500]]
- client contacts NS1, if name is not available NS1 suggests contacting NS2 and so on until name is resolved

### Server Controlled Navigation
#### Recursive Navigation
- performed by (any) naming server
- server becomes client for the next server
**Pros**
- necessary in case of client connectivity constraints; for security reasons. 

#### Non-Recursive Navigation
- performed by client or first server
- server bounces back next hop to client
![[Pasted image.png|500]]


-----------------
# References