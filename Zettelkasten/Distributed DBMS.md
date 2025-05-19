Created on: 06-05-2025 22:27
Status: #idea
Tags: #data_base #distributed_systems 
# Distributed DBMS
> Distribution of either the processing of data or the data  itself across multiple database environments

### DDBMS Components
- Computer Workstations
- Network hardware and software; to exchange data
- Transaction processor; that handles requests from application
- Data processor
	- Software resides on each workstation that retrieves and stores data
	- May be a centralized DBMS, if the data processor is on one computer which means we're distributing the data itself, while processing is centralized.
	- Communication between TPs and DPs are possible through protocols use by DDBMS.
### Pros
- Data is located near "greatest demand" site
- faster data access; if distributed database environment
- fault-tolerance; less danger of single-point of failure
- growth facilitation
- faster data processing (if distributed processing)
### Cons
- complexity
- security; have to secure each database
- lack of standards
- increase storage requirements
- increase training cost for new developers


-----------------
# References