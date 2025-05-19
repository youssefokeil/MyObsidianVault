Created on: 07-05-2025 02:20
Status: #idea
Tags: #distributed_systems 
# Message Passing Interface MPI
>Instead of shared memory, we make a layer of abstraction called interconnect. So each CPU reads data from the interconnect layer.

### MPI Functions
- `MPI_Init`
	start of scope
- `MPI_Finalize`
	end of scope
- `MPI_Comm_rank`
	know which process we're in, in number of processes
- `MPI_Comm_size`
	number of processes available
- `MPI_COMM_WORLD`
	variable gets specified, when you initialize MPI
- `MPI_Send`
	![[Screenshot From 2025-05-07 03-01-05.png]]
- `MPI_Recv`
	![[Screenshot From 2025-05-07 03-02-16.png]]
- `MPI_Bcast`
	broadcast message from root process to all other processes
```
int MPI_Bcast(void *buffer, int count, MPI_Datatype datatype,
int root, MPI_Comm comm)
```

-----------------
# References