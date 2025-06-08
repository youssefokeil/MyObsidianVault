Created on: 02-06-2025 19:35 
Status: #idea
Tags: #OS #computerscience 
# Locality of Reference
There are two types of locality

### 1) Temporal Locality
if a program accesses something in memory, it's highly likely that it will access it again in a very short time in the near future. 

_For t is access time of a variable:_

$$
t_{n+1}=t_{n}+\Delta
$$
$$\Delta : \text{is a very short time}$$

### 2) Spatial Locality
If a program accesses a part in the memory. It's highly likely that it will access an adjacent part.

_For A is accessed part in memory _
$$A_{n+1}=A_{n}+\Delta$$$$\Delta : \text{is a very small space}$$
-----------------
# References