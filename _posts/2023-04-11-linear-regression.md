---
layout: post
title: Linear Regression
date: 2023-04-11 11:12:00-0400
description: An Elementary Introduction to Linear Regressiion
categories: Machine-Learning
related_posts: true
---

__Linear Regression__ is a supervised machine learning model used to predict the value of one variable (a __prediction__, denoted $$\hat{y}^{i}$$) given the value of another variable (a __target__, denoted $$y^{i}$$). 

To obtain a prediction from a target, we need to have a training set composed of two columns: one for the input feature and one for the output variable. (In such a training set, each row or __training instances__ would correspond to a given house).

Let's suppose that our input feature is ''house size'' and our output variable is ''house price.'' In other words, let's try to predict a house's price based on its size. 


If we were to plot each training instance on a graph in the coordinate form (house size, house price), it is clear that there must exist a line of best fit which, by definition, minimizes the distance between itself and each point. Such a line can be derived from a __cost function__, which provides a measure of how well our ''prediction'' (the line itself) matches our ''target'' (the points). Such a measure is called the __cost__. The lower the cost, the better the fit of our line.)  

Since we want to use linear regression, we can use the following cost function J:

$$
J(w, b) = \frac{1}{2m} \sum_{i=1}^m (\hat{y}^{i} - y^{i})^{2}
$$,

where 
- $$w$$ and $$b$$ are __weights__ (coefficients whose values can be freely changed);
- $$m$$ is the __number of training instances__;
- $$x^{i}$$ is the __$$i^{th}$$ training instance__;
- $$\hat{y}^{i}$$ (sometimes written as $$f_{w, b}(x^{i}) or wx^{i}$$) is the __prediction__;
- and $$y^{i}$$ is a __target__.  

The portion $$\hat{y}^{i} - y^{i}$$ is called the __loss__. The fact that the cost function squares the loss ensures that the ''error surface'' is convex like a soup bowl. It will always have a minimum that can be reached by following the gradient in all dimensions.

Our goal is to minimize $$J(w, b)$$. (Think of it this way: The lower the value of $$J(w, b)$$, the better our linear line will fit the data.) Doing so requires that we find the ''optimal'' values of $$w$$ and $$b$$.



