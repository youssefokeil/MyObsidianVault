Created on: 24-03-2025 17:09
Status: #idea
Tags: #data_base 
# Database System
> The [[Database Management System (DBMS)]] with the data itself and sometimes it also includes the applications.

### Self-describing Nature
- DBMS catalog stores the description of a database (e.g. data structures, types and constraints)
- description is called meta-data
![[Screenshot 2025-03-24 172855.png|400]]

### Data Abstraction
- hide storage details and present users with a conceptual view
- Programs refer to relationships between data rather than data storage details
### Concurrency & Multi-users
- Allowing a set of concurrent users to retrieve and update the database 
- _Concurrency Control_
	- each transaction is correctly executed or aborted
	- ensure that several users are manipulating the same data in a controlled manner
- _Recovery subsystem_
	- each completed transaction has a permanent record in database
- OTLP online transaction processing
	- allows hundreds of concurrent transactions to execute per second

-----------------
# References