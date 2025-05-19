Created on: 06-05-2025 22:41
Status: #idea
Tags: #data_base #distributed_systems 
# Fragmentation
>Breaking single object into 2 or more fragments.
- Each fragment is stored on any site over a computer network
-  Transaction Processor accesses the _Distribute Data Catalog(DDC)_ which stores information on data fragmentation. 


### Types of Fragmentation
#### Horizontal Fragmentation
- split data by rows
#### Vertical Fragmentation
- split columns
- can split data across teams;
	- split customer information and account information into two DBMS
	- finance team only needs account information for example
#### Mixed Fragmentation
- a mixture of both horizontal and vertical information.



-----------------
# References