---
layout: post
title:      "Feature Scaling in python."
date:       2019-11-07 23:13:41 +0000
permalink:  feature_scaling_in_python
---


Data Science: Feature Scaling in python.

In our dynamic and ever-changing world of technology, data is like the lead artist. It sings beautiful songs, tell vivid stories and paint detail pictures based on factual truth embedded in numbers.  Like the old saying goes “Men lie, Women lie but numbers don’t lie”. In other words, numbers don’t change like the weather, number one is always number one and has been since the beginning of time however, data cannot just sing rhythmic melodies and draw colorful roadmap that points in the direction of the next big thing, you will have to tune it to get the best out of it, just like guitar and other musical instruments.

Data comes in different types, forms and shapes like apples and grapes, and when they do, its your job to **scale** them to fit the structure of the task at hand just like your music. 

So, let’s start with the question “What are features and what is Scaling”?

Basically, features are column names and the data under the respective columns that possess similar feature. For the most part these features usually have different magnitudes and quantitative measurements. Let’s look at a simple example. A column that contains height will have data measured in meters (m), the column that contains weight will have data measured in pounds (lbs) and the column that contains temperature will have data measured in Fahrenheit (F) or degrees Celsius (C).

Scaling is the process of altering the magnitude of the respective columns in a fixed ratio in order to unify its measurements without changing the shape of the data in question.

Do we have to use feature scaling all the time?

The direct answer to this question is NO, we do not have to use feature scaling all the time however, it is a great practice to do so since it accounts for the disparities in units and also help in reducing the expenses incurred as a result of computation.

In machine learning area, it does not only improve the performance of the model, it also reduces models from varying significantly.

What are the different types of feature scaling?

There are different scaling algorithm in Scikit-Learn for feature scaling. Some of which includes:

Standardization

Normalization

Min-Max Scaling

Robust Scaling

**Standardization:**

The most widely used scaling method is Standardization or StandardScaler.

The standardization method emphasizes on centering the data then dividing by the standard deviation so that the variable will have a standard deviation of one:

Xstd  = ( X - ¯X )/ Sx

Xstd  will have mean µ = 0 and Sx = 1


So, the coefficients of the predictors are in standard deviation units which allows direct comparison of magnitudes of different features.

StandardScaler transforms the data in such a way that the distribution has the mean value of zero (0) and standard deviation of one (1) as shown in the equation above.

We can see this in python using StandardScaler from Sklearn, the difference before standard scaler after standard scaler.

 
 
Before Standard Scaling and After Standard Scaling

**Normalization:**

This is the process of altering the variable magnitude “normalizing” to lie between 0 and 1. It is basically compressing the variable to a range of 0 and 1. 

This is achieved by dividing each value by its magnitude in n-dimensional space for n number of features.

Let’s say the features are x, y, z. the scaled value for x will look like this:

x_i/√(x_i^2+y_i^2+z_i^2 )

Now the points lie between 0 and 1.

**Min-Max Scaler:**

Min-Max Scaler is another scaling technique that transforms data so that it lies in the specified range. This is achieved by passing a tuple in the feature range parameter. Normally, it goes to default by selecting a range between 0 and 1.

It uses the minimum and maximum values for scaling so it is highly sensitive to outliers. 

Let’s take a look at the formula for calculating each feature:

((x_i-min⁡(x) ))/((max⁡(x)-min⁡(x) ) )

Let’s take a look at how it looks in python using sklearn:

 
Before Min-Max Scaling and After Min-Max Scaling

As we can see that the skewness is retained however the distribution of the 3 variables are transformed into the same scale.

**Robust Scaler:**

Robust scaler has a similar method to min-max scaling but instead of min and max, it uses interquartile range where Q1 and Q3 represents the quartiles.

In this method, the focus is more on the parts that have the most data, because of this, it is a great method for dealing with outliers.

Let’s look at the formula for robust scaler:

(x_i-Q_1 (x))/(Q_3 (x)-Q_1 (x) )

And this goes for every feature.
Let’s see how this looks like in python:

 
Before Robust Scaling and After Robust Scaling

As we can see, the outliers are left out while the distributions are within the same scale. Another major difference between min-max scaler and robust scaler beside the use of min, max for min-max scaler and quartiles for robust scaler is the distribution representation. 
Let’s go back to python to graphically see this difference.

 
Difference between “After Robust Scaling and After Min-Max Scaling

Clearly, we can see that in robust scaling, the distributions are within the same scale and overlap, however, the outliers remain on the outside of the majority of the scaled distribution.

For the Min-Max scaling, the normal distributions are between 0 and 1, and are kept separately from each other, separated by the outliers.

Conclusion 
These methods of data scaling are very instrumental to the preprocessing and preparation of data to be analyzed and visualized. When this is done, your data will have a better chance of vividly telling stories of the past and also painting a colorful roadmap to the next big thing by offering insightful details and trends that might be left out or missed during the process of preparing the data. 
There are other processes involve in processing and preparing data that are not mentioned in the post since this post is restricted to the importance of scaling and some of the methods used in scaling data.


