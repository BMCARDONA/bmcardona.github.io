---
layout: post
title: Linear Regression
date: 2023-04-11 11:12:00-0400
description: An Elementary Introduction to Linear Regressiion
categories: Machine Learning
related_posts: true
---

__Linear Regression__ is a supervised machine learning model used to predict the value of one variable (the __target__) based on the value of another variable (the __prediction__). For example, suppose that we are trying to predict the price of a home based on its size. The first step would be to compile a data set 

The __cost__ is the measure of how well our model predicts the target value. Moreover, we define a __cost function__ to be the performance of a machine learning model for a data set. 

Suppose we are given the following cost function:
$$
J(w, b) = \frac{1}{2m} \frac{1}{2m} \sum_{i=1}^m (\hat{y}^{i} - y^{i})^{2}, where
$$

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