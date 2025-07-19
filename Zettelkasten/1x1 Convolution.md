Created on: 17-04-2024 05:12
Status: #idea
Tags: #AI/CNN #AI/fastai #AI/computer_vision 
# 1x1 Convolution
Most successful CNN architectures use 1x1 Convolution. Ex: GoogleNet, ResNet, SqueezeNet.
1x1 Conv is used to reduce number of channels while introducing non linearity (this is called Cross Channel Down Sampling).

![[1_dNaikOfrGzUaJ2EzRIl4tw.webp|600x400]]

By choosing a 1x1 filter (with no of channels=number of filters). This keeps the same HxW but decreases the number of channels.

## Uses:
1. Dimensionality reduction and in turn decrease the computational load on the model; used in the Inception Module
	![[w_o_1x1_conv.webp]]
	![[with_1x1.webp]]
	by using a 1x1 convolution in the beginning we decrease the number of channels and this causes the number of computations to decrease by a factor of 10.

2. Deeper networks, using "Bottleneck Layers". In bottleneck layers, we diminish then restore the number of channels and still not impact the performance of the model that much.
	![[att_00045.png]]

3. Edge Computing. In things like autonomous driving cars, we need the model to be as fast as possible. That's why we use things like the Fire Modules which are used in SqueezeNet. Those modules have so much less parameters than vanilla ConvNets.
-----------------
# References
[[Deep Learning For Coders]], [[1X1 Convolution, CNN, CV, Neural Networks | Analytics Vidhya (medium.com)](https://medium.com/analytics-vidhya/talented-mr-1x1-comprehensive-look-at-1x1-convolution-in-deep-learning-f6b355825578)]