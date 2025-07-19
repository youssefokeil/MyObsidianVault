Created on: 18-09-2024 14:23
Status: #idea
Tags: #AI/computer_vision #AI 
# Harrison corner detector
>is a method to extract corners of an image
### Steps:
1. Convert images to grayscale images. 
2. Extract I_x and I_y by convolving with [[Sobel Operators]].
3. Take I_x and I_y and compute a matric that looks like this:
![[Screenshot 2024-09-18 145521.png]]
4. Measure response of each pixel
$$
\begin{equation*} R = \operatorname{det}(M)-k \operatorname{tr}(M)^{2} . \end{equation*}
$$
5. Set threshold and find pixels that are above this threshold. 
6. (Optional) You'd typically dilation to extract and display the pixels.
### Code:
```
# Convert to grayscale
gray = cv2.cvtColor(image_copy, cv2.COLOR_RGB2GRAY)
gray = np.float32(gray)

# Detect corners 
dst = cv2.cornerHarris(gray, 2, 3, 0.04)

# Dilate corner image to enhance corner points
dst = cv2.dilate(dst,None)
```

-----------------
# References
[[Computer Vision Nanodegree]]