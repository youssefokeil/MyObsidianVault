Created on: 29-03-2024 08:52
Status: #idea
Tags: #computer_vision #CNN #AI #fastai #temporal_data
# Average Pool
> Is a [[Pooling]] (down-sampling) operation that takes patches of data to output a smaller grid size, helpful to reduce the dimensions of a feature map, without adding new parameters to learn or heavier computation.

 ## **Parameters:** 
 - pool size: specifying how big our pooling window should be
 - strides: meaning how much should our pooling window move after each operation
## Average Pool 2-D
takes the average over the grid defined by x-, y- axes. Pool size is a tuple.
![[Avg-Pooling.png]]
## Average Pool 1-D

![[Max-and-average-pooling-with-a-1D-filter.png]]
## Problems 
The problem with average pooling and any pooling layer is being so satisfied with their accuracy and using it everywhere, however, they're just a good choice for objects with no one correct orientation or size:
- It doesn't make sense in OCR(optical character recognition) such as MNIST because you're effectively taking slices of images, seeing if it looks like a 3 or 8 and averaging that over all slices.
### See also
 [[Max Pool]]
-----------------
# References
[[Deep Learning For Coders]]