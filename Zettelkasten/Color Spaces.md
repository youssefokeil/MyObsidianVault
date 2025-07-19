Created on: 18-08-2024 16:06
Status: #idea
Tags: #AI #preprocessing #AI/computer_vision 
# Color Spaces
> is a color mode to represent digital data into images or vice versa. The point is having a mutual understanding of an encoding to images, so that they can easily be transferred using digital data.

## Types of Color Spaces:
- RGB: the most famous one, encodes images in 3 primary colors red, green and blue
- HSV( also called HSB): hue, saturation and value (brightness), it's useful when trying to isolate parts of images in specific color(hue) and not wanting the brightness or the shading affect that.
- CMYB: cyan, magenta, yellow and black. Used in printing processes.

## Transformations:
transforming from one color space to another may seem hard, but it's easy using various libraries.
```
# cv2.cvtColor() is used to convert from one color space to another
new_img= cv2.cvtColor(src=old_img,code=<specific_code>)
```
#### Different codes
 - always used when loading imgs because opencv loads in default BGR
	`cv2.COLOR_BGR2RGB` 

- HSV is always useful when needing to extract parts with specific color, agnostic of brightness
	`cv2.COLOR_RGB2HSV`




-----------------
# References
[[Computer Vision Nanodegree]]