Created on: 22-10-2024 00:10
Status: #idea
Tags: #electronics #digital_circuits 
# NMOS Regions of Operation
### 1. Subthreshold (cut-off ) Region:
$$
\begin{aligned}
V_{GS}<V_{TH}\\
I_{D}<< \text{"very small"}
\end{aligned}
$$
### 2. Triode Region:
$$\begin{aligned}
V_{GS}>V_{TH} \\
V_{DS}< MIN(V_{OV}, V_{Sat})\\
V_{sat}\text{  is because of the drift velocity saturation}
\end{aligned}$$
$$
I_{D}=\frac{1}{2}*\mu_{n}*C_{ox}*\frac{W}{L}(2(V_{GS}-V_{TH})*V_{DS}-V_{DS})^2
$$
### 3. Saturation Region:
$$\begin{aligned}
V_{GS}>V_{TH} \\
V_{DS}>MIN(V_{OV},V_{SAT})
\end{aligned}
$$
$$
I_{D}=\frac{1}{2}*\mu_{n}*C_{ox}*\frac{W}{L}(V_{GS}-V_{TH})^2
$$

![[nmos-char.gif]]

-----------------
# References
[[Digital Circuits]]