---
layout: distill
title: Eigendecomposition of a Real Symmetric Matrix
giscus_comments: false
date: 2023-04-23

authors:
  - name: Bradley Cardona
    # url: "https://en.wikipedia.org/wiki/Albert_Einstein"
    # affiliations:
    #   name: IAS, Princeton

bibliography: deep-learning.bib # To change bibliography, go to assets --> bibliography


# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Equation
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Example
#   - name: Footnotes
#   - name: Code Blocks
#   - name: Interactive Plots
#   - name: Layouts
#   - name: Other Typography?

# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }

---

## Equation

On page 42 of *Deep Learning* by Bengio et al, it is stated that every symmetric matrix $A$ can be decomposed into an expression using only real valued-eigenvectors and eigenvalues, such that
$$
A = Q \Lambda Q^T \tag{2.41}
$$
where $Q$ is an orthogonal matrix composed of eigenvectors of $A$, and $\Lambda$ is a diagonal matrix. The eigenvalue $\Lambda_{i,i}$ is associated with the eigenvector in column $i$ of $Q$, denoted as $Q_{:,i}$. 

## Example

Here's an example of a real symmetric matrix that can be decomposed into an expression using only real-valued eigenvectors and eigenvalues:

Let's say we have a 2x2 real symmetric matrix `A`:
$$
A = \begin{bmatrix}
2 & -1 \\
-1 & 2
\end{bmatrix}
$$
The characteristic polynomial of `A` is given by:
$$
|A - \lambda I| = \begin{vmatrix}
2 - \lambda & -1 \\
-1 & 2 - \lambda
\end{vmatrix} = (2-\lambda)^2 - 1 = \lambda^2 - 4\lambda + 3
$$
The eigenvalues of `A` are the roots of the characteristic polynomial:
$$
\lambda^2 - 4\lambda + 3 = 0 \Rightarrow (\lambda - 1)(\lambda - 3) = 0 \Rightarrow \lambda_1 = 1, \lambda_2 = 3
$$
The eigenvectors of `A` are given by solving the equation `(A - λI)v = 0` for each eigenvalue `λ`. For `λ_1 = 1`, we have:
$$
(A - \lambda_1 I)v_1 = \begin{bmatrix}
1 & -1 \\
-1 & 1
\end{bmatrix}v_1 = 0 \Rightarrow v_1 = t\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$
For `λ_2 = 3`, we have:
$$
(A - \lambda_2 I)v_2 = \begin{bmatrix}
-1 & -1 \\
-1 & -1
\end{bmatrix}v_2 = 0 \Rightarrow v_2 = t\begin{bmatrix}
-1 \\
1
\end{bmatrix}
$$
Thus, the eigenvectors of `A` are `v_1 = [1, 1]` and `v_2 = [-1, 1]`. We can normalize these eigenvectors to obtain an orthogonal matrix `Q`:
$$
Q = \frac{1}{\sqrt{2}}\begin{bmatrix}
1 & -1 \\
1 & 1
\end{bmatrix}
$$
The diagonal matrix `Λ` is given by:
$$
Λ = \begin{bmatrix}
\lambda_1 & 0 \\
0 & \lambda_2
\end{bmatrix} = \begin{bmatrix}
1 & 0 \\
0 & 3
\end{bmatrix}
$$
Thus, we have decomposed `A` into the expression:
$$
A = QΛQ^T = \frac{1}{\sqrt{2}}\begin{bmatrix}
1 & -1 \\
1 & 1
\end{bmatrix}\begin{bmatrix}



