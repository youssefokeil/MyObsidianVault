Created on: 14-08-2024 15:25
Status: #idea
Tags: #websites
# Resize Images before save
> Don't save images with original resolution, if you already need a small part of it/resized part of it.

Ex:
	if you are saving profile pictures, you'll probably have a CSS resize to 125x125 image for example. You don't need to save in your file system the whole image but the 125x125 resized image to save up space
### Algorithms:
```
from PIL import Image

new_img = Image.open(original_image)
output_size=(125,125) #whatever size you want
new_img.thumbnail(output_size) #creates thumbnail of img smaller than original
new_img.save(path_to_image)
```





-----------------
# References