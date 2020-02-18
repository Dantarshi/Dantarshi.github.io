---
layout: post
title:      "Random Forest Model"
date:       2020-02-18 21:33:52 +0000
permalink:  random_forest_model
---



What is a random forest model?
Random forest is simply a bundle of decision trees and it makes sense why it called random forest. Literally a forest is a collection of multiple trees to make a forest. For us to have a true understanding of a random forest, we will need to understand the concept of decision trees.
Take a look at the diagram below, let say the blue and green dots in the diagram are represent trees in a forest. If a tree is added in the top right part of this forest, what do you suggest the color of the tree will be? 
I’m thinking that you are thinking green and you are right about it.

 

Decision tree is something we go through every single day as long as we get to make a decision.
Random forest is a supervised machine learning algorithm used to predict an outcome, this outcome can be numerical (also known as regression) or represent a class (also known as classification). Random forest models do not necessary make assumptions with regards to the distribution of the data or any specific parameters so we regard it as a non-parametric model. 
Random forest has the ability to combine many underlying models to vote for one and we refer to that method as “ensemble learning method”. We can see 
 
The combination of these underlying model which are also know as decision trees make up a model known as Random forest.
Let’s take a graphical look at what we just discussed earlier on.
 
For each decision tree, there is a subset with similar but distinctive data points. These splits determine how we learn about our data. The better our split is, the more we learn from our data and the measure of the effectiveness of our split is called “Information gain”.

Decision trees are usually considered as “weak learners”, this is because they are not complex model and are slightly better than a random chance outcome so combining these weak learners together forms a solid model.
Advantages of random forest:
1.	It does not have any problems with large datasets
2.	It has the ability to generalize internal unbiased estimate of error in building a forest.
3.	It has the ability of handling missing data and still produce a high level of accuracy.
4.	It is one of the most accurate machine learning algorithms and it can produce a pretty high accurate classifier as well.
5.	It also provides level of importance of the variables.
Disadvantages of Random forest:
1.	Random forest has a tendency to overfit if the dataset has a reasonable amount of noise during a classification or regression.
2.	When dealing with categorical variables, random forest has more bias in favor of those attributes with a greater level.
What is the logic behind random forest?
Random forest consists of two important phases, training and testing phases. The training phase is responsible for creating the forest and the testing phase is responsible for making the predictions from the test data that is fed into or model.



