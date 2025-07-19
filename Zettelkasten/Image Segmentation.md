Created on: 19-07-2025 18:11, note by Youssef Okeil
Status: #idea
Tags: #AI/computer_vision 
# Image Segmentation
> **Discontinuity:** partition image into regions based on abrupt changes in intensity, such as edges.
> **Similarity**: partitioning image into regions that are similar based according to set of predefined features.

## Mathematical Background
for *R* is the entire spatial region occupied by an image. It can be segmented into *n* subregions: *R1, R2, ..., Rn*
![[Pasted image 20250719212421.png]]
- point(a), means that the segmentation must be complete, that every pixel must be in a region.
- point(c) represents that there is no overlap between subregions, that regions are *disjoint*.
- If the union of two subregions is connected then they are adjacent.
- point(d) refers to the properties that must be satisfied by the pixels in a segmented region, for example if all pixels in Ri have the same color.

![[Pasted image 20250719220040.png]]
- a-->c represents segmentation based on pixel intensity.
- d-->f segmentation based on standard deviation as a predicate. It is nonzero, where there is texture and zero otherwise.
-----------------
# References
[[Digital Image Processing]]