Created on: 31-05-2025 16:16 
Status: #idea
Tags: #software #BaRead 
# CRUDs
> way to link between use cases & classes. To know how each use case affects a class. It can also map between classes.
- It can be class-by-class tables
- or case-by-class tables
- filled with one or more letters from CRUDs (create, read, update, delete) to show interaction between use-cases/classes with other classes.
### Example
**Use cases**: create order, dispatch order, create customer, modify customer, update stock (add new item) and increase stock.
**Classes**: customer, phone, address, purchase order, order item, item stock.

|                                 | customer | phone       | address | purchase order | order item | item stock |
| ------------------------------- | -------- | ----------- | ------- | -------------- | ---------- | ---------- |
| **create order**                | R        |             |         | C              | C*         | R          |
| **dispatch order**              | R        |             | R       | R              | R*         | U*         |
| **create customer**             | C        | C*          | C       |                |            |            |
| **modify customer**             | U        | U\*/C\*/D\* | U       |                |            |            |
| **update stock (add new item)** |          |             |         |                |            | C          |
| **increase stock**              |          |             |         |                |            | U          |
\* : means multiple

-----------------
# References