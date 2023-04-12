---
layout: post
title: Linear Regression
date: 2023-04-11 11:12:00-0400
description: An Elementary Introduction to Linear Regression
categories: Machine-Learning
related_posts: true
---

__Linear Regression__ is used in supervised machine learning to build a mathematical model that describes the relationship between the input features and the output variables in a training set. 

To create such a model, we would need a training set composed of (say) two columns: one for the input feature and one for the output variable. (We can actually have as many input features as we want; for simplicity, however, I will I will stick with just one input feature.) Let's suppose that our input feature is ''house size'' and our output variable is ''house price.'' (Hence, each row or ''training instances'' corresponds to a given house). If we were to plot each training instance on a graph in the coordinate form (house size, house price), then there must exist a best-fit line which, by definition, minimizes the distance between itself and each point. Such a line can be derived from a __cost function__ which provides a measure of how well our ''prediction'' matches our ''target.'' Such a measure is called the __cost__. (The lower the cost, the better the fit of our line.)  

Since we want to use linear regression, we can use the following cost function J:

$$
J(w, b) = \frac{1}{2m} \sum_{i=1}^m (\hat{y}^{(i)} - y^{(i)})^{2}
$$,

where 
- $$w$$ and $$b$$ are __weights__ (coefficients whose values can be freely changed);
- $$m$$ is the __number of training instances__;
- $$x^{(i)}$$ is the __$$i^{th}$$ training instance__;
- $$\hat{y}^{(i)}$$ (sometimes written as $$f_{w, b}(x^{(i)})$$ or $$wx^{(i)}$$) is the __prediction__;
- and $$y^{(i)}$$ is a __target__.  

The difference $$\hat{y}^{(i)} - y^{(i)}$$ is sometimes referred to as the __loss__. The fact that the cost function squares the loss ensures that the ''error surface'' is convex like a bowl. It will always have a minimum that can be reached by following the gradient in all dimensions.

Our goal is to minimize $$J(w, b)$$, which requires that we find the ''optimal'' values of $$w$$ and $$b$$. The lower the value of $$J(w, b)$$, the better our linear line will fit the data.



