---
layout: post
title:      "Data Visualization Using Matplotlib"
date:       2020-04-06 11:52:30 -0400
permalink:  data_visualization_using_matplotlib
---



The amount of data generated today is mind blowing. Data come in different types however, we will need to present them in a way that a non-technical audience can make meaning out of it and make decisions based on the data that is presented to them. 
A great way to capture, analyze and communicate data is through the use of Python. Now, what is Python?
 Python is one of the powerful tools used in the data science ecosystem. It has powerful libraries that can enable us to create detail visualizations that are compelling and ready for both technical and non-technical audience.
Why do we use a programming language (Python)?
We use python as a programming language that can enable us to do a lot of different types of visualization, these includes boxplots, bar graphs, line graphs, histogram, et cetera. 
Using a programming language like Python allows us to build data visualization that can iterate and improve the quality of our visualization.
Data visualization is simplifying data, cleaning data to help stakeholders understand the information hidden in raw data which can be useful for decision making.
We are in a very difficult time as I write this blog, we are dealing with a novel virus called coronavirus, it is a virus that we do not understand because we have never seen something like this before. We do not have data for it so we can not make a sound judgement or gain insight about it from historical data.
 We are collecting data as we go and this drives down the point of why data is so important to our survival. 
Collecting data all over the world alone will not provide any meaningful insight, we will have to clean the data, present it in such a way that it can make sense even to a non-technical audience.
Python uses many libraries to handle data visualization, some of these libraries include:
1.	Mathplotlib
2.	Pandas built in Visualization library
3.	Plotly and Cufflinks
4.	Seaborn
5.	Geographical plotting.
However, we will stick to Matplotlib for now. 
Matplotlib is a Python library used to create wonderful figures in 2D (Two-Dimension), it supports interactive and hard copy formats as well. Matplotlib works on many IDE’s (Integrated Development Environment) such as IPython, Web application Servers, Python Script, and Jupyter Notebook.
Matplotlib was originally designed to simulate Matlab graphical plotting but for python users, it gives them a lot of control over all aspect of visualization and for that reason it is one of the most popular plotting libraries for python.
How do we plot in Matplotlib?
First, we have to import the library by using 
 “import pandas as pd”
“import numpy as np”
“import matplotlib.pyplot as plt”
Numpy library also known as ‘Numerical Python’ is used for scientific computing, Pandas library is a used for data manipulation and analysis, and as we already know, matplotlib is used for data visualization.
We have two styles to plot in matplotlib,  
1.	 Matlab-style (Functional method)
2.	 Object-Syntax (Object-Oriented method)

Matlab-Style (Functional Method)
Remember to use plt.show() at the last line when using python script.
Let’s say x is the variable inputs and y is the target values,
1.	Plt.plot(x,y), there are other parameters that we can add to create an interesting visualization  such as color, size etc
2.	Plt.xlabel(“Text”) this sets the x-axis label 
3.	Plt.ylabel(“Text”) this sets the y-axis label
4.	Plt.set_title(“Text”) this allocate a title to the current axes
5.	Plt.show() used to display the figure.
 

Object-syntax (Object -Oriented Style)
Object syntax is another way to write the codes for the creation of visualization. We create an object figure and call a method to it. We use syntax like .figure() method. After the figure is created, we set the axes by calling the .add_axes() method.
Let’s use the same x and y values earlier.
1.	Fig = plt.figure() used to create a figure
2.	Axes = fig.add_axes() used to add axes to the figure, you can pass in whatever quantity you want to adjust the width and height.
3.	Axes.plot(x,y) used to plot y versus x 
4.	Axes.set_xlabel(‘Text”) sets the x-axis label
5.	Axes.set_ylabel(“text) sets the y-axis label
6.	Axes.set_title(“text) sets the title of the axes
 
There are a lot of things that can be added to the plot to improve it. Some of those customizations include: 
Grid lines, colors etc. This can be achieved by adding plt.grid() for matlab syntax then specify the axis you want the gridlines to appear on and for object-oriented syntax we can simply use axes.grid(), and we can also pass in whatever specification we want.
we can use matplotlib to do a lot of data visualizations, let’s try scattered plot.

 
As we can see from the code, we used only matplotlib, the scatter plot shows points all over the place because we used the rand() function and not randint so it generated random floating points with  numbers <= 1.

Let’s take another look at a basic histogram.

[picture]

 
The histogram shows the frequency distribution, we got 200 random numbers between 0 and 30 and used the object-oriented syntax to plot the bar chart.

Let’s look at another type of chart that we can plot with matplotlib, pie chart.
We will provide labels on this pie chart just to show how matplotlib gives you a lot of control over your figure. The labels have to be in same order as the data else matplotlib will not figure out how to place the labels correctly.

 

How can we save our plots?
Using the matlab style we can save our files using plt.savefig() and we can pas in where we want to save it and the dpi as resolution. 
Matplotlib flaws 
Matplotlib is very popular for data visualization library however, it has its own flaws.
There are no gridlines, has a white background, it is a very low-level library so it takes a lot of codes to do any complicated task, it lacks integration with pandas data structures which makes it very inconvenient. To get around this with use matplotlib wrappers like seaborn and pandas.

Conclusion
Matplotlib is a powerful library that does great visualization and does even complex task if used with wrappers like pandas and seaborn.


