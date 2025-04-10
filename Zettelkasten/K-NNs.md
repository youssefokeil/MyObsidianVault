Created on: 10-07-2024 23:36
Status: #idea
Tags: #computer_vision #AI 
# k-NNs Nearest Neighbor
### Trains:
> by memorizing all data and labels. O(1) constant time as it only assigns pointers.
### Predicts:
>Compares image to be predicted with all images and finds most similar training image. O(N) linear time, compares image to each of the training data.

### Hyperparameters:
1. Distance metric.
2. Value of K. Look at [[Finding Hyperparameter]].
### Pros:
- Very easy to interpret because it's simple.
- High Accuracy for large datasets
- Good for nonlinear data, makes no assumption on data.
- _**Universal Approximation:** _
	As number of training examples goes to infinity, KNNs can represent any function.
### Cons:
- Parameter to find is K. Expensive to find if dataset is large.
- Prediction is slow for large datasets.
- Not meaningful in a perceptional way.
- Very sensitive to data's scale and irrelevant features.
- Doesn't handle high dimensionality (large number of features and attributes).
	***Curse of Dimensionality:***
	for uniform coverage of space, number of parameters exponentially grows.
	Ex:
			dim(1)=4 points, dim(2)=4^2 ,dim(3)=4^3 
		






-----------------
# References
[[Deep Learning For Computer Vision]]