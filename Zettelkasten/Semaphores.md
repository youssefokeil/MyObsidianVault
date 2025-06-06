Created on: 28-05-2025 22:03 
Status: #idea
Tags: #OS
# Semaphores
> is a more robust tool for synchronization than [[Mutex Locks]]. It was created by Dutch computer scientists Edsger Dijkstra

1. We have an integer variable S
2. we have `wait()` atomic operation
3. we have `signal()` atomic operation
### Types:
- binary semaphores --> exactly like [[Mutex Locks]]
- counting semaphores --> range over an unrestricted domain
-------------
## Busy-waiting:
### Wait
```
wait(S) {	
	while (S <= 0)
		; // busy wait
	S—;
}
```
### Signal
```
signal(S) {
	S++;
}
```
-----------------
## Suspend/Sleep
### Semaphore
```
typedef struct { int value;
	struct process *list;
} semaphore;
```
### wait
--> each process suspends itself & adds itself to the buffer queue of the semaphore,
--> `value` can be negative & its magnitude indicates the number of processes waiting on the semaphore
```
wait(semaphore *S) {
	S->value—; 
		if (S->value < 0) {
			add this process to S->list; 
			sleep();
	}
}
```
### signal
--> the wake-up call resumes operation of the suspended process
```
signal(semaphore *S) {
	S->value++; 
	if (S->value <= 0) {
		remove a process P from S->list; 
		wakeup(P);
	}
}
```

#### How to ensure atomic operations?
- On uni-core systems 
	- disable interrupts during the `wait()` & `signal()` execution. All other processes can't be interleaved, while the current process is executes until interrupts are re-enabled.
- On multi-core systems 
	- disabling interrupts on every core can be very difficult. It usually uses spin locks or [[Compare & Swap]].
	- Despite not eliminating busy-waiting totally, we have moved the busy-wait from the entry section to the critical-section (which should be at most 10 operations).
-----------------
# References