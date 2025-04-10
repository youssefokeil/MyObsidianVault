Created on: 02-09-2024 00:19
Status: #idea
Tags: #networks
# Priority Scheduling
> Is a buffer management algorithm. Classifies buffered packets into classes, using the header fields, it then sends packets from highest priority queue first.

### Rules:
- High priority class is served before low priority classes
- FIFO within classes
- If a packet is in service, we don't interrupt it if a higher priority class packet arrives. We first finish serving it then serve the higher priority class.

![[Screenshot 2024-09-02 003512.png|400]]





-----------------
# References
[[Computer Networks]]