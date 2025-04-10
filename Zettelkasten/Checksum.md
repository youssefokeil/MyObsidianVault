Created on: 13-08-2024 14:23
Status: #idea
Tags: #networks 
# Checksum
>Used to detect data corruption
### Steps:
**At sender:**
1. Break original message into k blocks, where each block has n bits. 
	Ex: 20 bit message is divided into 4 blocks of 5 bits each
2. Sum all k blocks
3. Add carry to sum
4. Do 1's complement to sum and this equals the checksum
 **At receiver:**
 1. repeat steps of sender
 2. add checksum to sum of all data blocks
 3. if all sum of all data segments and checksum, outputs a data of all 1 bits, then there was (probably)  no corruption.




-----------------
# References
[[Computer Networks]]