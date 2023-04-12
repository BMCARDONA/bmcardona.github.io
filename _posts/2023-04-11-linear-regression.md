---
layout: post
title: Linear Regression
date: 2023-04-11 11:12:00-0400
description: An Elementary Introduction to Linear Regression
categories: Machine-Learning
related_posts: true
---

__Linear Regression__ is used in supervised machine learning to build a mathematical function that describes the relationship between the input features and the output variables in a training set. 

To create such a function, we need a training set composed of (say) two columns: one for the input features and one for the output variables. (We will actually have several columns if we have several input features; for simplicity, though, we will assume in this article that we are dealing with just one input feature.) 

Let's suppose that in our training set our input feature is ''house size'' and our output variable is ''house price.'' (Hence, each row or ''training instance'' of our training set corresponds to a single house). Our goal then is to create a mathematical function that describes the relationship between house sizes and house prices. 

If we were to plot each training instance on a graph in coordinate form, i.e., in the form (house size, house price), then there should exist a best-fit line which minimizes the distance between itself and each point. Such a line can be derived from a __cost function__, which provides a cumulative measure of how well each ''prediction'' matches each ''target.'' (In this example, a ''prediction'' is the output variable that results from our function when we ''feed it'' an input feature. The ''target'' is the output variable in our training set associated with that given input feature.) This measure is called the __cost__. The lower the cost, the better the fit of our line.

Since we want to use linear regression to create this function, we can use the following cost function J:

$$
J(w, b) = \frac{1}{2m} \sum_{i=1}^m (\hat{y}^{(i)} - y^{(i)})^{2}
$$,

where 
- $$w$$ and $$b$$ are __weights__ (coefficients whose values can be freely manipulated);
- $$m$$ is the __number of training instances__;
- $$x^{(i)}$$ is the __$$i^{th}$$ training instance__;
- $$\hat{y}^{(i)}$$ (sometimes written as $$f_{w, b}(x^{(i)})$$ or $$w\cdot x^{(i)} + b$$) is the __prediction__;
- and $$y^{(i)}$$ is the __target__.  

Note: The difference $$\hat{y}^{(i)} - y^{(i)}$$ is sometimes referred to as the __loss__. The fact that the cost function squares the loss ensures that the ''error surface'' is convex like a bowl. It will always have a minimum that can be reached by following the gradient in all dimensions.

Our goal is to minimize $$J(w, b)$$, which requires that we find the ''optimal'' values of $$w$$ and $$b$$. The lower the value of $$J(w, b)$$, the better our line will fit the data.



