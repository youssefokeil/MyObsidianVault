Created on: 10-04-2025 17:37
Status: #idea
Tags: #software
# Software Design
>Determines the principal code units of a software system.


```
class BankAccount {
  private Customer customer;
  private double balance;
  public double getBalance() { ... }
  public String getCustomerName() { ... }
  public String getStatement(Date start, Date end) { ... }
  ...
}
```
### Provided Interfaces:
Services that a code unit makes public for other parts of the system.
- In the above example, `BankAccount` provides services to other classes through public methods `getbalance(), getCustomerName(),..` thus constituting a provided interface

### Required Interfaces:
Code unit depends on for operation. 
- `Customer` is a required interface for `BankAccount` as `BankAccount` depends on `Customer`.



-----------------
# References
[[Software Engineering:  A Modern Approach]]