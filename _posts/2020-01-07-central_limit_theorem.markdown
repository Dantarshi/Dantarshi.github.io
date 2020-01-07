---
layout: post
title:      "Central Limit Theorem"
date:       2020-01-07 16:45:03 +0000
permalink:  central_limit_theorem
---


Data Science: Central limit Theorems
What is central limit theorem?
The central limit theorem states that the sampling distribution of the mean of any independent or random variable will be normal or almost nearly normal if the sample size is large enough.
The next question one will ask is, how much sample is large enough?
The answer to this question will depend on basically two important factors.
1.	The acceptable requirement for accuracy. So, if you want an almost near normal distribution then you will require more sample points and so as the sample points size increases, the tendency of producing a normal distribution increase as well.
2.	The next factor is the shape on the population that we are looking at. This has everything to do with the original population in consideration, if the original population looks like a normal distribution then you will not have to worry much about more sample points because we will need less sample points to create a normal distribution that will satisfy the central limit theorem.
Different people from different statistical back ground have various suggestion on the sample size, some say 30 is large enough, others say 40 is large enough and others say 50 is the ideal number however, if the original population distribution is far from normal with rough bell shape, terribly skewed with multiple peaks and exaggerated outliers then the recommended number given by all these statisticians about the ideal sample points size and its sample distribution will not work for a given population.

Let us take a look at the mathematical representation of a classical central limit theorem.

We will consider certain factors that are crucial to the central limit theorem. 
Let Xn   be an independent sequence of identically distributed random variables.
Lets also assume that X has a finite mean, E(X) = μ, finite variance, Var(X) = σ2.
Let’s give Zn to be normalized average of the 1st n random variables, so we can mathematically represent this as:
	Zn = (X1 + X2 + … + Xn – nμ)/ σ √ n.
Now classical central limit theorem will say that Zn converges to a standard normal distribution.
Basically, this is saying that cumulative distributed function (CDF) of Zn converges to  Φ , which is the standard normal (Gaussian) random variable.

Now we will dive into python for a better explanation and visualization of how the central limit theorem looks like.  
Let’s use some codes as well to illustrate how central limit theorem works.
To fully appreciate the central limit theorem, we will visualize it in python using anaconda jupyter notebook. We will create random samples of travel bags weighing between 50 to 80 lbs, each of size n = 40 and we will visualize the sample distribution. Once this is done, we will run a simulation multiple times (1000)  to collect the sample means and visualize it as well to see if the distribution resembles a normal distribution.
Here are the codes:
from numpy.random import seed
from numpy.random import randint
from numpy import mean
# seed the random number generator, so that the experiment is #replicable
seed(1)
# generate a sample of men's weights
weights = randint(50, 80, 40)
plt.hist(weights)
plt.show();
print(weights)
print('The average weight is {} lbs'.format(mean(weights)))
 

[55 61 62 58 59 61 55 65 50 66 51 62 57 63 78 56 75 68 70 55 68 70 61 78
 60 78 79 64 68 54 73 73 59 67 73 50 72 63 59 59]
The average weight is 63.875 lbs

As we can see the sample distribution is not close to normal.
We will now run it multiple times (1000)  and document the means so that we can visualize it also.
Here are the codes:
import matplotlib.pyplot as plt
# seed the random number generator, so that the experiment is replicable
seed(1)
# calculate the mean of 50 men's weights 1000 times
means = [mean(randint(50, 80, 40)) for _i in range(1000)]
# plot the distribution of sample means
plt.hist(means)
plt.show();
print('The mean of the sample means is {}'.format(mean(means)))
 
The mean of the sample means is 64.54
To be really sure of or normal distribution, we will run a normality test on our data. Let’s use normality check to test by using a statistical library in python called Scipy.
so let’s come up with a hypothesis to test this theory.
Our hypothesis is given below:
H0: data follow a normal distribution
H1: data do not follow a normal distribution
We will set out alpha to be 0.05 with is the level of confidence for this test.
The code is below:
print(stat.normaltest(means))
result: NormaltestResult(statistic=3.7254251559933107, pvalue=0.15525092842446248)


if you look at the result of our pvalue it is 0.1552509284244
Since the p-value is greater than our confidence level apha (it is much greater than significant level of alpha) we fail to reject the null hypothesis that states that data follow normal distribution.
We can increase the sample size n a couple of times, so n=60 , then 70 then 75 and we will run the same codes to see if any changes occur:
n = 60, pvalue = 0.57544

 
n = 70, pvalue = 0.26834
 
As we can see, the higher we increase the sample size n, the higher the pvalue increases and subsequently the higher the confidence with which we can not reject the null hypothesis of our normality test which states that data follow normal distribution. 
Conclusion 
The central limit theorem is extremely important when dealing with data that is heavily skewed with multiple peaks and extraordinary outliers. With the use of central limit theorem, we can some what tame the data which will help us perform analysis and draw reasonable information out of the data which in turn help with decision making. Central limit theorem is one of the great tools data scientist use to have a grip on a data that is all over the place. Some statistician use all methods of scaling to attain normality with their data too as well.
Reference
•	https://www.investopedia.com/terms/c/central_limit_theorem.asp
•	http://mathworld.wolfram.com/CentralLimitTheorem.html
•	https://www.analyticsvidhya.com/blog/2019/05/statistics-101-introduction-central-limit-theorem/
•	https://towardsdatascience.com/visualizing-the-central-limit-theorem-with-python-e89d2ce41788
Written by 
Ice Asortse

