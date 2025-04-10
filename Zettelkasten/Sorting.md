Created on: 25-11-2024 07:21
Status: #idea
Tags: #data_structures #algorithms 
# Sorting
Sorting is a very important computational problem in data structures, that is important in on of itself but is also used as a building block to solve bigger computational problems.
- Binary Search
- Removing duplicates
- Balancing data structures to ensure faster operations

### Mental Model (1): The Ordering Relation "<"
the [[Ordering relation]] is a relation to sort elements in a set. For our narrow case we'll use Don Knuth's definition
- _Law of trichotomy:_ either a<b, b>a, a=b. Only one of them is true
- _Law of transitivity:_ if a<b & b<c, then a<c.

#### NB:
> This mental model is important because in lots of programming languages, all you need to define is the ordering relation, and the sorting is handled by a function/method already defined. 

__Ex:__
- In Cpp you pass the function that compares to `algorithm::sort()`.
### Mental Model (2): Inversions:
another useful mental model for sorting is inversions. Inversions are two elements that are not in order according to the ordering relation defined.
- Maximum number of inversions for n elements is $$n\choose2$$
- The goal is to minimize number of inversions to zero by the end of the algorithm.
- Some algorithms work by increasing the number of inversions first, and some are monotonic and in each step decrease the number of inversions.



-----------------
# References
[[Data Structures by Berkeley]]