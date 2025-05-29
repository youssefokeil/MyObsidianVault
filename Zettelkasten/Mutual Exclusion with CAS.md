Created on: 29-05-2025 00:41 
Status: #idea
Tags: #OS
# Mutual Exclusion with CAS
- `lock` is initialized to 0
- first process that invokes `lock` will set it to 1, as (`lock==0`) --> enter critical-section
- subsequent calls to `compare_and_swap()` will not succeed
- when a process ends critical-section, it set `lock` to 0 --> allow other processes to enter critical section.
```
while (true) {

	while (compare_and_swap(&lock, 0, 1) != 0) ; 
		/* do nothing */
		
		/* critical section */
	
	lock = 0;
	
		/* remainder section */
}
```
### Problem:
This doesn't satisfy bounded-waiting. Any process can take critical section two times in a row.

-------------------
### Mutual-Exclusion Bounded-Waiting with CAS
1. Mutual Exclusion is met:
	 process enters critical section only if --> 
	 - `waiting[i]==false` (another process left critical section)
	 - or `key==0` (compare and swap is executed)
2. Progress is met
	- when a process exits critical section --> sets `lock` to 0 & `waiting[j]` to false 
	- both allow any waiting process to enter critical section
3. Bounded-waiting is met 
	- a process leaves its critical section, it scans the array waiting in the cyclic ordering ( i + 1, i + 2, ..., n - 1, 0, ..., i - 1)
	- first process where (`waiting[j]==true`) is the next one to enter critical-section
	- Any process waiting to enter critical section will thus do in *n -1*  turns.
```
while (true) {

	waiting[i] = true; 
	key = 1;	
	while (waiting[i] && key == 1)
		key = compare_and_swap(&lock,0,1); 
	waiting[i] = false;
	
		/* critical section */
	
	j = (i + 1) % n; 
	while ((j != i) && !waiting [j]) 
		j = (j + 1) % n;
	
	if (j == i) 
		lock = 0; 
	else
		waiting [j] = false;
	
		/* remainder section */
}
```

-----------------
# References