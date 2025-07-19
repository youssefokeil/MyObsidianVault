Created on: 19-07-2025 22:36, note by Youssef Okeil
Status: #idea
Tags: #AI/computer_vision 
# Point, Line & Edge Detection
> Segmentation methods that are based on detecting sharp, local changes in intensity. Points, lines and edges. 

*Edge pixels* are pixels at which the intensity of image changes abruptly
1. *Edge Detectors* are local image processing tools designed to detect edge pixels.
2. *Line* can be viewed as a thin edge segment in which the intensity on either side is much lower or much higher than the intensity of the line.
3. *Isolated Point* may be viewed as foreground pixel surrounded by background pixels.
The changes in intensity can be detected using derivatives. Here we'll use the *Taylor series*.
![[Taylor Series#Taylor Series]]

### First-order derivative
We however use an approximation of the Taylor series, by using only the linear terms.
1. forward difference
$$\frac{\partial f(x)}{\partial x} = f^{'}(x) = f(x+1)-f(x)$$
2. backward difference
$$\frac{\partial f(x)}{\partial x} = f^{'}(x) = f(x)-f(x-1)$$
3. central difference
$$\frac{\partial f(x)}{\partial x} = f^{'}(x) = \frac{f(x+1)-f(x-1)}{2}$$
The error between the exact and the approximate  can be decrease by adding more terms of the Taylor Series, however central differences have lower error for same number of points. That's why derivatives are usually expressed as central differences.
### Second-order derivative 
Second order derivative is based on a central difference, $$\frac{\partial ^ {2}f(x)}{\partial x ^{2}=}f(x+1)-2f(x)+f(x-1)$$
the point to find even the third and fourth derivatives, is to combine Taylor expansions to eliminate all derivatives above the third or fourth derivatives respectively.
![[Pasted image 20250720003524.png]] First four central derivatives coefficients.

-----------------
# References
[[Digital Image Processing]]