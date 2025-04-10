Created on: 21-10-2024 14:44
Status: #idea
Tags: #digital_circuits #electronics 
# Implementation Choices
in digital circuits, you have to choose between a full-custom vs a semi-custom design
### 1. Full-Custom:
You design each and every component from scratch.
__Importance:__
- someone has to design and implement libraries
- adequate model of cells is needed for standard cells
- redesigning standard cells for new constraints of cost and power
- Troubleshooting requires circuit expertise

### 2. Semi-Custom:
choose between:
- Cell-based: where you implement your design by taking indivisible cells and connect them together. 
	Choose between Macro-cells and standard cells
- Array-Based: have arrays of millions of cells and interconnect needed cells.
	[[FPGA]]s and pre-diffused arrays




-----------------
# References
[[Digital Circuits]]