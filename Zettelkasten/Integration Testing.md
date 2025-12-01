Created on: 12-11-2025 17:16, note by Youssef Okeil
Status: #idea
Tags: #software 
# Integration Testing
> verifies that logically integrated modules work correctly as a group.
- Detect interface defects after integration.
- Update tests for new or changed requirements.
- Validate db connections and data flow.
- Ensure proper exception handling across modules.

![[Pasted image 20251112180220.png]]
## Integration Testing Approaches
1. **Big-Bang**: Integrate all modules at once & tests them as a unit.
==**Advantages**==
	- Convenient for small systems
==**Disadvantages**==
	- *Hard to localize faults*
	- Some interfaces may be missed
	- limited time for testing after all modules are ready
	- Critical & UI modules may lack priority.
2. **Top-Down:** Start from top-level modules, use stubs for lower ones.
==**Advantages**==	
	- needs many stubs
	- *easier fault localization*
	- *Possibility for an early prototype*
	- Critical modules are tested first
==**Disadvantages**==
	- *needs many stubs*
	- Modules at lower level are tested inadequately
3. **Bottom-Up** Start from lower-level modules, use drivers for upper ones.
==**Advantages**==
	 - *easier fault localization*
	- Concurrent development saves time
==**Disadvantages**==
	- *No early prototype*
	- critical modules tested last
4. **Sandwich** Hybrid of top-down and bottom-up
==**Advantages**==
	 - good compromise for large projects
==**Disadvantages**==
	- *difficult to design and write*

-----
## Pros:
- even if units work individually, they may fail when combined. Because of:
	- Mismatched data formats
	- Incorrect assumptions
	- Poor exception handling

----
# References
[[Courses/Software Testing|Software Testing]]