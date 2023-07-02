---
layout: post
title: Linear Algebra in a Neural Network Layer
date: 2023-06-09 16:42:00-0400
categories: ["Machine Learning", "Deep Learning"]
related_posts: false
---

It can be difficult to wrap one's mind around what is happening computationally inside the layer of a neural network between an input matrix, a weight matrix, and a bias vector. Let's go through an example to see exactly how to calculate the dot product between an input matrix $$\mathbf{\hat{X}}$$ and a weight matrix $$\mathbf{\hat{W}}$$, how broadcasting is used to add the bias vector $$\mathbf{\hat{b}}$$ to the resulting dot product, and why the dimensions of the resulting matrices and vectors make sense. 

Suppose we have an $$2 \times 2$$ input matrix $$\mathbf{\hat{X}}$$, which represents a batch of 2 training examples, with 2 features each:

$$
\mathbf{\hat{X}} = \begin{bmatrix}
1 & 2 \\\\
3 & 4
\end{bmatrix}.
$$

Suppose that $$\mathbf{\hat{X}}$$ serves as the input to a layer with 3 units (neurons). We will therefore have a $$2 \times 3$$ weight matrix $$\mathbf{\hat{W}}$$, where 2 is given by the number of features of $$\mathbf{\hat{X}}$$, and 3 is given by the number of units in the current layer:

$$
\mathbf{\hat{W}} = \begin{bmatrix}
0.1 & 0.2 & 0.3 \\\\
0.4 & 0.5 & 0.6
\end{bmatrix}.
$$

By taking the dot product of $$\mathbf{\hat{X}}$$ and $$\mathbf{\hat{W}}$$, we are left with a $$2 \times 3$$ matrix:

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

Let's assume we have a $$1 \times 3$$ bias vector $$\mathbf{\hat{b}}$$ (where 3 is given by the number of units in the current layer), representing the bias for each unit in the layer:

$$
\mathbf{\hat{b}} = \begin{bmatrix}
0.7 & -0.8 & 0.9
\end{bmatrix}.
$$

We will use broadcasting to expand $$\mathbf{\hat{b}}$$. (Broadcasting applies to element-wise operations.
Its basic operation is to 'stretch' a smaller dimension by replicating elements to match a larger dimension. In this case, we will 'stretch' $$\mathbf{\hat{b}}$$ by replicating its rows, so that it has a size of $$2 \times 3$$, the same dimensions as $$\mathbf{\hat{X}} \cdot \mathbf{\hat{W}}$$.) Let's call this broadcasted matrix $$\mathbf{\hat{B}}$$. We have 

$$
\mathbf{\hat{B}} = \begin{bmatrix}
0.7 & -0.8 & 0.9 \\\\
0.7 & -0.8 & 0.9
\end{bmatrix}.
$$

We can now add $$\mathbf{\hat{B}}$$ element-wise to $$\mathbf{\hat{X}} \cdot \mathbf{\hat{W}}$$:

$$
\mathbf{\hat{X}}\mathbf{\hat{W}} + \mathbf{\hat{B}} = \begin{bmatrix}
0.9 + 0.7 & 1.2 - 0.8 & 1.5 + 0.9 \\\\
1.7 + 0.7 & 2.4 - 0.8 & 3.1 + 0.9
\end{bmatrix} = \begin{bmatrix}
1.6 & 0.4 & 2.4 \\\\
2.4 & 1.6 & 4
\end{bmatrix}.
$$

<!-- Hence, broadcasting just involves adding the bias vector $$\mathbf{\hat{b}}$$ element-wise to each row of the resulting matrix from the dot product of $$\mathbf{\hat{X}}$$ and $$\mathbf{\hat{W}}$$. -->

It is worth pointing out that the resulting matrix has a size of $$2 \times 3$$ (which is the same as $$\mathbf{\hat{X}} \cdot \mathbf{\hat{W}}$$), where $$2$$ is given by the number of features of $$\mathbf{\hat{X}}$$, and $$3$$ is given by the number of units in the current layer. 

For completeness, here is a vectorized implemention of the example in Python: 
```python 
import numpy as np

def dense(X, W, b):                  # dense layer
    z = np.matmul(X, W) + b          # np.matmul() returns the matrix product of two matrices
    return z

X = np.array([[1, 2],                # batch
              [3, 4]])
W = np.array([[0.1, 0.2, 0.3],       # weights
              [0.4, 0.5, 0.6]])
b = np.array([[0.7, -0.8, 0.9]])     # biases

result = dense(X, W, b)
return result
```

We may generalize this example by saying that the dimensions of the parameters in a given layer are determined as follows:
- If network has $$s_{in}$$ units in a layer (i.e., if each training example of $$\mathbf{\hat{X}}$$ has $$s_{in}$$ features) and $$s_{out}$$ units in the next layer (i.e., if the current layer has $$s_{out}$$ units/neurons), then 
    - $$\mathbf{\hat{W}}$$ will be of dimension $$s_{in} \times s_{out}$$.
    - $$\mathbf{\hat{b}}$$ will be a vector with $$s_{out}$$ elements
- Note: A layer's input dimensions ($$s_{in}$$) are calculated for you. You specify a layer's output dimensions and this determines the next layer's input dimension. The input dimension of the first layer is derived from the size of the input data specified in the model.fit statement

**As an aside**:
It need not be said that I initially had trouble keeping track of the dimensions of the matrices and vectors found in a layer of even a basic neural network. My hope is that this post will provide some insight into how to perform a basic linear algebra computation inside a neural network layer, and why the dimensions of the various vectors and matrices involved make sense. I am currently completing Andrew Ng's Advanced Learning Algorithms class on Coursera, and will likely use this post as a reference in the months to come.