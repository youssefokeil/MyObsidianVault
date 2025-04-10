Created on: 18-08-2024 12:11
Status: #idea
Tags: #networks
# Classic TCP Congestion Control
Additive Increase Multiplicative Decrease, sender increases transmission rate(window size), until loss occurs
- Additive increase:  increase congestion window (cwnd) by 1 MSS every RTT
- Multiplicative decrease: cut cwnd by half after loss detected

![[A-line-graph-showing-the-default-Saw-Tooth-behaviour-of-the-TCP-Protocol-with.png]]

### Why additive increase?





-----------------
# References
[[Computer Networks]]