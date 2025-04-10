Created on: 11-07-2024 01:15
Status: #idea
Tags: #AI #computer_vision 
# Finding Hyperparameter
### Idea 1:
choose parameters that work best on training set:
**Bad Idea:**
- will work so much better than the model is. (Ex: in [[K-NNs]] will choose K=1 and it will work perfectly, because each image can match a training image exactly(which is the same image) )
### Idea 2
Split data into train & test. Choose parameters that work best on test set:
**Bad Idea:**
- will get an accuracy better than how the model performs.
- the point is for the model to predict well on data it hasn't seen. By making decisions using the test set, then the model has seen the test set.
## Idea 3
Split into train, validation and test
- A very practical approach and used a lot by practitioners

## Idea 4
Using cross-validation: Split  data into folds, try each fold as validation and average over all.
- The best approach, but takes lots of computation
- Used for small datasets.





-----------------
# References
[[Deep Learning For Computer Vision]]