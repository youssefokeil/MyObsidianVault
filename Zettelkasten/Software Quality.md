Created on: 10-04-2025 21:50
Status: #idea
Tags:
# Software Quality
A classification by Bertrand Meyer suggests that Software Quality can be evaluated in two dimensions
### 1. External Quality
factors that can be evaluated without examining the source code.
- Correctness: Does the software align with its specification and perform as expected under normal conditions?
    
- Robustness: Can the software continue to function appropriately during exceptional circumstances, such as communication or disk failures? A robust software system should not crash due to such events; instead, it should alert users about the abnormal operation.
    
- Efficiency: Is the software making optimal use of the available computational resources?
    
- Portability: Is the software adaptable to other platforms and operating systems? Is it available for major operating systems? Does it run on mobile devices?
    
- Ease of Use: Does the software have a user-friendly interface, clear error messages, and support for multiple languages? Can users with disabilities, such as visual or auditory impairments, use it?
    
- Compatibility: Does the software support the most common data formats in its domain? For instance, a spreadsheet should import files in XLS and CSV formats.
### 2. Internal Quality
Relates to properties associated with the system's implementation
- Modularity
- Code readability
- Maintainability
- Testability
### Strategies for Assurance of  Software Quality
- Metrics 
	to track the development process, Ex:
	- Number of lines of a program, which provides an indication of its size.
	- Process metrics, which includes the number of bugs reported by end-users over a specific period.
- Code Reviews
	Code written by one developer on developer only moves to production after another team member reviews and approves it. This aids:
	- Early bug detection, before system enters production
	- Contributes to improving the quality of the code (readability, maintainability)




-----------------
# References
[[Software Engineering:  A Modern Approach]]