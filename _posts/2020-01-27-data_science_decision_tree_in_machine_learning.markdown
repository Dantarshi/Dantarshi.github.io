---
layout: post
title:      "Data Science: Decision Tree in machine learning."
date:       2020-01-27 16:57:21 -0500
permalink:  data_science_decision_tree_in_machine_learning
---



What is a Decision tree? 
Generally, we can define decision tree as a decision supporting tool that uses a tree-like model of decisions with regards to the possibility of consequences, including resource cost, utility and outcomes. It is one of the many ways to visualize algorithm that are based on conditions and statements.
Machine Learning with Decision tree?
When dealing with machine learning, we view decision tree as a non-parametric supervised learning method which is used for both classification and regression task or analysis. This has a specific goal which is to predict the value of target variable by learning the rules involved in simple decision inferred from data features.
A non-parametric method simply means that the model does not have any assumptions of data distribution of errors or the data itself.
A good example of decision tree is when a bank or financial institution what’s to offer someone a credit card, they often follow a sequential list of items to find out the risk involved in doing business with that potential customer, in other words, they want to know if it is safe to offer a credit card to that individual. 











Let take a look at the diagram


                                        <$30k                                                                                 >$70k
                                                                            $30-70k


Yes                  No                                           <1                1-5          >5                                       No                  Yes






                                                           Yes                                                  No       


Like mentioned earlier on, decision tree is mostly a non-parametric mechine learning modeling technique for both regression and classification problems. It is also based on hierarchical sequence meaning there are queston asked in sequence that determine the classification of the outcome. Basically model based on observed data.
Decision tree machine learning has the abilty to enhance our decisions based on factual data.  It help us create a logical and mathematical rules to generate selection based on intuition and subjectivity.
Algorithm
When dealing woth decision tree, algorithm becomes the next question.
We can define algorithm as the set of rules used to solve a particular problem.
What is decision tree algorithm?
Decision tree algorithm is simply a supervised learning algorithm that can be used for solving regression and classification problems.
Types of decision trees:
Decision trees are typically based on two types:
	Categorical variable decision tree: which is simply a decision tree that has a categorical variable as the target variable.
	Continuous variable decision:  this is the decision tree that has continuous variable as a target variable.

Decision tree terminologies:

	Decision Node: when a sub-node splits into more sub-nodes then it is called decision node.
	Root Node: the root node is the representation of the entire population or samples and can be further divided into more homogeneous sets.
	Parent and Child Node: any node that is divided into sub-nodes is referred to as a parent node and the sub-nodes are called child of the parent node.
	Leaf/Terminal Node: any node that does not split any further is called the leaf or terminal node.
	Branch? Sub-tree: the subsection of the entire tree can be referred to as branch or sub-tree.
	Splitting: splitting is the process of dividing the node into two or more sub-nodes.
	Pruning: pruning is simply the removal of sub-nodes of the decision tree, it is practically the opposite of splitting.

Some assumptions about decision tree
These are some of the assumptions we usually make when using decision tree:
	The training set is considered as the root.
	Most of the feature values are preferred to be categorical, in case they are continuous, they are discretized before building a decision tree model.
	Records are distributed recursively based on the attribute’s values.
	A statistical approach is used to determine the placing pf attributes as roots or internal node on the tree. 
Normally we have two attribute selection measures:
	Information gain
	Gini index
Information Gain
when a node is used in a decision tree to partition the training instances in to smaller subsets, there is a change in entropy. This will lead us to ask what entropy is? 
Entropy is the measure of uncertainty of a random variable. So, information gain is the measure of change in entropy.
Let us see how it looks like mathematically:
Suppose S is a set of instances, A is an attribute, Sv is the subset of S with A = v, and Values (A) is the set of all possible values of A, then
Gain(S,A) = Entropy(S) - ∑vevalues(A))|s_v |/|s| ⋅ Entropy(Sv).
Gini Index
Gini index is a metric to measure the frequency of randomly chosen element would be incorrectly identified. The lower the “Gini” the better or the more preferred.
Let us see how it works mathematically;
Gini Index = 1 - Σ_j P_j^2
Advantages of Decision tree:
	Decision trees are very easy to interpret because it comes as a result of some set of rules.
	It has about the same approach when it comes to the process used by human beings in decision making.
	Visualization can easily simplify a very complex model of decision tree to a point that a non-technical audience can easily understand or interpret.
	It has practically no hyper-parameter tuning.
	Decision tree can handle both numerical and categorical data.
	Decision tree is resistant to outliers and can require little data processing.
Disadvantages of Decision Tree:
	The probability of overfitting is very high if care is not taking, which will fail to generalize.
	A categorical variable can give a biased response for attributes with a greater number of categories in the information gain.
	In general, decision tree has a lower prediction accuracy for a dataset compared to other machine learning algorithms.
	If there are many class labels, calculation might become complex and time consuming.

Conclusion
There are many applications of decision tree in machine learning that have real life impact directly.  This blog is only an introduction to the basics of decision tree, the important terminologies, the instances and basically how decision tree works.
References

	https://towardsdatascience.com/decision-tree-in-machine-learning-e380942a4c96
	https://www.geeksforgeeks.org/decision-tree-introduction-example/
	https://medium.com/@sagar.rawale3/understanding-decision-tree-algorithm-drawbacks-and-advantages-4486efa6b8c3

