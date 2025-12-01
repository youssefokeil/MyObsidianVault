Created on: 12-11-2025 15:20, note by Youssef Okeil
Status: #idea
Tags: #software 
# Unit Testing
> Unit testing is the process of testing the smallest testable unit of an application (a function, method, procedure, module, or object) to validate that each unit performs as expected.
-----
In the V-Model, it comes before the [[Integration Testing]]
![[The V-Model#The V-Model]]

Unit Testing can be automated using Unit Test Frameworks, like [[JUnit]] for Java, to develop automated test cases.

---
## Mock Objects
> Simulated object that mimics the behavior of real components.

- Isolate the unit under test
- Replace dependencies that are external or complex (e.g., database, API)
- Enable testing in controlled conditions
- Has same interface as the real component
- Provides predefined responses to method calls
-  Does not perform real operations (e.g., no actual DB queries)
-----
## Pros
- *Makes debugging easier, helps in finding bugs early and saves cost*
- *help developers understand the code better*
- Serve as project documentation
- Help with code re-use as they migrate both code and tests to be used for new project.
----
## Cons:
- Poorly execution of unit testing can be a waste of resources and money
- *It adds to initial development time*
- *Too many tests increase maintenance overheads*
- Redundant or incomplete tests can create false confidence in code quality
-----------------
# References
[[Courses/Software Testing|Software Testing]]