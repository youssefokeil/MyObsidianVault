Created on: 06-06-2025 18:39 
Status: #idea
Tags: #data_base 
# Relationships (Database)
> relates two or more distinct entities with a specific meaning.

### Degree of a Relationship
1. Binary Relationship:
	- is between two entities
	- Manages *manages* a Department
2. Ternary Relationship
	- links three entities.
	- Supplier *supplies* a Part
	- Part is *supplied* for a project
3. Recursive Relationship
	- Relationship between an entity & itself
	- Worker *supervises* other workers
### Cardinality of Relationships
The number of 
1. One-to-one Relationship
	- one entity has a *relationship* with only one entity.
	- One Employee *manages* one department.
2. One-to-many Relationship
	- 1:M
	- One Department *manages* multiple (M) projects
	- Each project is *managed* by at most one Department
3. Many-to-many relationship
	- M:N
	- Employee can *work* in multiple projects
	- Project contains *multiple* projects

### Participation Constraints
1. Total participation
	- all entities in a relationship  *must* participate in a relationship
	- Represented as double-lines ===
2. Partial Participation
	- relationship where not all entities have to be in the relationship
	- represented with single-line ----

### EXTRA: Min-Max Notation
- Minimum is usually 
	- 1 --> means total-participation
	- 0 --> means partial-participation
- Maximum can constraint number of entity involved in a relationship



-----------------
# References