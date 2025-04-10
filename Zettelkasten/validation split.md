Created on: 02-10-2023 19:14
Status: #idea
Tags: #kaggle #deeplearning 
# validation split
**_Making a good validation split is half of your work on a project. To do so you have to:_**
- According to the dataset and the project. Determine how to split your data. Randomly? Stratified? According to a timestamp?
#### For Kaggle competitions.
**_You'll want not only for the split to be good, but you want it to track the leaderboard score:_**
 - Ideally, the results will align with the leaderboard(LB) results.
 - It's enough if the results move in the same direction as LB (increase/decrease).
 - Make 2 models as a bare minimum. Submit both and see if local results are like the LB. If not, review your split!
-------
#### Things to [[check]]:
- [Learning From Data: A short course](https://work.caltech.edu/telecourse) A book and MOOC by Yaser S. Mostafa




-----------------
# References
[[Metalearning]]