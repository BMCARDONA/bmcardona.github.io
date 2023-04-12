---
layout: post
title: Linear Regression
date: 2023-04-11 11:12:00-0400
description: An Elementary Introduction to Linear Regressiion
categories: Machine-Learning
related_posts: true
---

__Linear Regression__ is a supervised machine learning model used to predict the value of one variable (a __target variable__) given the value of another variable (a __prediction__). For example, let's suppose that our target variable is ''house price'' and our prediction is ''house size'' To predict the former from the latter, we first would need to obtain a training set composed of several rows (each row corresponding to a given house) and two columns, namely, ''house price'' and ''house size.'' 


If we plot each row of this training set in coordinate form (house price, house size), it should be clear that there must exist a line of best fit which minimizes the distance between it and each coordinate. Such a line can be derived from a __cost function__, which provides a measure of how well our ''prediction'' (the line itself) matches our training data (the points). (Specifically, the cost function tells us the __cost__, which is the measure of how well our model predicts the target value. The lower the cost, the better the fit of the line.)  

Since we want to use linear regression, we can use the following cost function J:
$$
\[ J(w, b) = \frac{1}{2m} \sum_{i=1}^m (\hat{y}^{i} - y^{i})^{2} \]
$$,

where $$w$$ and $$b$$ are __weights__ (a coefficient that we can freely change), $$m$$ is the __number of training instances__, $$i$$ is the __$$i^{th}$$ training instance__, $$x^{i}$$ is a __training instance__, $$\hat{y}^{i}$$ (sometimes written as $$f_{w, b}(x^{i}) or wx^{i}$$) is the __prediction__, $$y^{i}$$ is a __target__.     

Our goal is to minimize $$J(w, b)$$. The lower the value of $$J(w, b)$$, the better our linear line fits the data. 



<!-- This theme supports rendering beautiful math in inline and display modes using [MathJax 3](https://www.mathjax.org/) engine. You just need to surround your math expression with `$$`, like `$$ E = mc^2 $$`. If you leave it inside a paragraph, it will produce an inline expression, just like $$ E = mc^2 $$.

To use display mode, again surround your expression with `$$` and place it as a separate paragraph. Here is an example:

$$
\sum_{k=1}^\infty |\langle x, e_k \rangle|^2 \leq \|x\|^2
$$

You can also use `\begin{equation}...\end{equation}` instead of `$$` for display mode math.
MathJax will automatically number equations:

\begin{equation}
\label{eq:cauchy-schwarz}
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
\end{equation}

and by adding `\label{...}` inside the equation environment, we can now refer to the equation using `\eqref`.

Note that MathJax 3 is [a major re-write of MathJax](https://docs.mathjax.org/en/latest/upgrading/whats-new-3.0.html) that brought a significant improvement to the loading and rendering speed, which is now [on par with KaTeX](http://www.intmath.com/cg5/katex-mathjax-comparison.php). -->