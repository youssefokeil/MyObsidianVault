Created on: 29-05-2025 00:44 
Status: #idea
Tags: #OS 
# Mutex Locks
> is an OS solution to the [[Critical-Section]] problem. Is the simplest solution.

- It has a boolean variable --> indicates if lock is available or not.
- If lock is available --> call to `acquire()` succeeds, this makes the lock unavailable & all other processes that wants to acquire lock are blocked
- `release()` --> releases the lock for other processes
```
while (true) {
	acquire lock
		critical section
	
	release lock
		remainder section
}
```
### Acquire
```
acquire() {
	while (!available)
		; /* busy wait */ 
	available = false;
}
```

### Release
```
release(){
	available=true;
}
```
### Problems:
- it requires busy-waiting
	- wastes CPU cycles
- This implementation is called spin-lock --> preferable because it decreases context-switching, used for short-duration locking. 
-----------------
# References