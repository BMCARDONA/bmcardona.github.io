---
layout: post
title: The Basic Linear Algebra of a Neural Network Layer
date: 2023-06-09 16:42:00-0400
categories: ["Machine Learning"]
related_posts: false
img: assets/img/neural_network.jpeg
---

It is sometimes difficult to wrap one's mind around what is happening mathematically inside the layer of a neural network between an input matrix, a weight matrix, and a bias vector. But, fear not! Let's go through an example to see *exactly* how the dot product between an input matrix $\mathbf{\hat{X}}$ and a weight matrix $\mathbf{\hat{W}}$ is calculated, how broadcasting can be used to add the bias vector $\mathbf{\hat{b}}$ to the resulting product, and why the dimensions of the resulting matrices and vectors make sense. 

Suppose we have an $2 \times 2$ input matrix $\mathbf{\hat{X}}$, which represents a batch of 2 training examples, with 2 features each:

$$
\mathbf{\hat{X}} = \begin{bmatrix}
1 & 2 \\\\
3 & 4
\end{bmatrix}.
$$

Suppose, moreover, that $\mathbf{\hat{X}}$ is the input of a layer with 3 units (neurons). We will therefore have a $2 \times 3$ weight matrix $\mathbf{\hat{W}}$, where 2 is given by the number of features of $\mathbf{\hat{X}}$, and 3 is given by the number of units in the current layer:

$$
\mathbf{\hat{W}} = \begin{bmatrix}
0.1 & 0.2 & 0.3 \\\\
0.4 & 0.5 & 0.6
\end{bmatrix}.
$$

By taking the dot product of $\mathbf{\hat{X}}$ and $\mathbf{\hat{W}}$, we are left with a $2 \times 3$ matrix:

$$
\begin{aligned}
\mathbf{\hat{X}} \cdot \mathbf{\hat{W}} &= \begin{bmatrix}
1 \cdot 0.1 + 2 \cdot 0.4 & 1 \cdot 0.2 + 2 \cdot 0.5 & 1 \cdot 0.3 + 2 \cdot 0.6 \\\\
3 \cdot 0.1 + 4 \cdot 0.4 & 3 \cdot 0.2 + 4 \cdot 0.5 & 3 \cdot 0.3 + 4 \cdot 0.6
\end{bmatrix} \\
&= \begin{bmatrix}
0.9 & 1.2 & 1.5 \\\\
1.7 & 2.4 & 3.1
\end{bmatrix}.
\end{aligned}
$$

Now, let's assume we have a $3 \times 1$ bias vector $\mathbf{\hat{b}}$ (where 3 is given by the number of units in the current layer), representing the bias for each unit in the layer:

$$
b = \begin{bmatrix}
0.7 \\\\
-0.8 \\\\
0.9
\end{bmatrix}.
$$

Using broadcasting, we can add the bias vector $\mathbf{\hat{b}}$ to each row of the resulting dot product matrix:

$$
\mathbf{\hat{X}}\mathbf{\hat{W}} + \mathbf{\hat{b}} = \begin{bmatrix}
0.9 + 0.7 & 1.2 - 0.8 & 1.5 + 0.9 \\\\
1.7 + 0.7 & 2.4 - 0.8 & 3.1 + 0.9
\end{bmatrix} = \begin{bmatrix}
1.6 & 0.4 & 2.4 \\\\
2.4 & 1.6 & 4
\end{bmatrix}.
$$

Hence, broadcasting just involves adding the bias vector $\mathbf{\hat{b}}$ element-wise to each row of the resulting matrix from the dot product of $\mathbf{\hat{X}}$ and $\mathbf{\hat{W}}$.

It is worth pointing out that the resulting matrix has a size of $2 \times 3$, where $2$ is given the the number of training examples in the current batch, and $3$ is given by the number of units in the current layer. 

**As an aside**:
It need not be said that I initially had trouble keeping track of the dimensions of the matrices and vectors found in a layer of even a basic neural network. My hope is that this post will provide insight into how some basic linear algebra computations are performed inside a layer, and why the dimensions of the various vectors and matrices involved make sense. I am currently completing Andrew Ng's Advanced Learning Algorithms class on Coursera, and will likely use this post as a reference in the months to come.
