Created on: 20-04-2025 11:44
Status: #idea
Tags: #software
# Non-Functional Requirements
>The constraints bunder which the system should operate 

- Outline _how_ a system should operate.
- Constraints and the quality of service.


#### Quality Attributes
|**Non-Functional Req.**|**Metric**|
|---|---|
|Performance|Transactions per second, response time, latency, throughput|
|Space|Storage usage, RAM, cache usage|
|Reliability|Uptime percentage, Mean Time Between Failures (MTBF)|
|Robustness|Mean Time To Recover (MTTR) after a failure, risk of data loss after a failure|
|Usability|User training time|
|Portability|Percentage of portable lines of code|
### Specification
It's better to avoid unclear specifications like "system should be fast and have high availability". 
__Instead you should define that the system should__
- ensure 99.99% availability
- that 99% of transactions should be conducted in 5-minute windows.

-----------------
# References
[[Software Engineering:  A Modern Approach]]