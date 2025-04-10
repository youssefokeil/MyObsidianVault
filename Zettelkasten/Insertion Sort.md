Created on: 26-11-2024 08:21
Status: #idea
Tags: #data_structures #algorithms #sorting
# Insertion Sort
is a [[Sorting]] algorithm, that is computationally expensive but is used for small lists or lists that are nearly sorted.
## Used for:
- Small arrays. For small arrays, insertion sort is probably the fastest algorithm. That's why java's implementation of mergesort uses insertion sort for arrays less than 15 elements.
- Nearly sorted arrays. For sorted arrays the algorithm takes O(N). For nearly sorted arrays with K inversions, it takes O(N+K)
_______
## Implementation:
#### Naive Insertion Sort:
Create a new array, that is empty at first. Then take each element from original array and insert it one by one at its correct position. Check this [cs61b naive insertion sort demo](https://docs.google.com/presentation/d/181Lhn8jf4N-VG1BOkV4-Caj1wKcavkls8fnTKJlCuXc/pub?start=false&loop=false&delayms=3000&slide=id.g463de7561_042).
#### In-place Insertion Sort:
Instead of creating a new array. We move from left to right and in each pass we select a "traveler" , by swapping that element backwards until it finds its position among previously examined elements. Check this [cs61b in-place insertion sort demo](https://docs.google.com/presentation/d/10b9aRqpGJu8pUk8OpfqUIEEm8ou-zmmC7b_BE5wgNg0/edit#slide=id.g463de7561_042).

![[Screenshot 2024-11-26 084248.png]]
____________
### Complexity:
__Time Complexity:__
- Best: for sorted array $$O(N)$$
- Average: $$O(N^2)$$
- Worst: $$O(N^2)$$
_____________________________
__Space Complexity:__
- For in-place: $$O(1)$$
- For Naive: $$O(N)$$
-----------------
# References
[[Data Structures by Berkeley]]