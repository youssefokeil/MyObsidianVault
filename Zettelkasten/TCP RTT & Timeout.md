Created on: 17-08-2024 16:23
Status: #idea
Tags: #networks 
# TCP RTT & Timeout

### How to set TCP timeout value?

It has to not be too short, so we get premature timeout and not too long so we have slow reaction to segment loss. The way to specify a timeout, is by looking for a good RTT.

### How to measure RTT?
- SampleRTT: measures time from segment transmission until ACK receipt. 
- EstimatedRTT: Average RTT of  over several recent measurements.
$$
\begin{aligned}
EstimatedRTT=(1-\alpha)*EstimatedRTT+ \alpha*SampleRTT \\
\alpha =0.125
\end{aligned}
$$

### Measuring timeout:
it's the EstimatedRTT plus a safety margin, as larger deviation happends, the larger otu safety margin should be.
$$
\begin{aligned}
DevRTT=(1-\beta)*DevRTT+ \beta*|SampleRTT-EstimatedRTT|
\\ \beta=0.25
\\ TimoutInterval=EstimatedRTT+4*DevRTT 
\end{aligned}
$$


-----------------
# References
[[Computer Networks]]