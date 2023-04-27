---
layout: distill
title: Eigendecomposition of a Real Symmetric Matrix
giscus_comments: false
categories: ["Machine Learning"]
date: 2023-04-23
img: assets/img/linear-regression.png
---

authors:
  - name: Bradley Cardona

bibliography: deep-learning.bib # To change bibliography, go to assets --> bibliography

toc:
  - name: Equation
  <!-- - name: Citations -->
  - name: Example

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

where $Q$ is an orthogonal matrix composed of eigenvectors of $A$, and $\Lambda$ is a diagonal matrix. The eigenvalue $\Lambda_{i,i}$ is associated with the eigenvector in column $i$ of $Q$, denoted as $Q_{:,i}$.<d-cite key="Goodfellow-et-al-2016"></d-cite> 

***

<!-- ## Citations

Citations are then used in the article body with the `<d-cite>` tag.
The key attribute is a reference to the id provided in the bibliography.
The key attribute can take multiple ids, separated by commas.

The citation is presented inline like this: <d-cite key="Goodfellow-et-al-2016"></d-cite> (a number that displays more information on hover).
If you have an appendix, a bibliography is automatically created and populated in it.

Distill chose a numerical inline citation style to improve readability of citation dense articles and because many of the benefits of longer citations are obviated by displaying more information on hover.
However, we consider it good style to mention author last names if you discuss something at length and it fits into the flow well — the authors are human and it’s nice for them to have the community associate them with their work.

*** -->

## Example

Here's an example using a 2x2 real symmetric matrix:

Let's say we have a 2x2 real symmetric matrix `C`:

$$
C = \begin{bmatrix}
4 & 1 \\
1 & 4
\end{bmatrix}
$$

The characteristic polynomial of `C` is given by:

$$
|C - \lambda I| = \begin{vmatrix}
4 - \lambda & 1 \\
1 & 4 - \lambda
\end{vmatrix} = (4-\lambda)^2 - 1 = \lambda^2 - 8\lambda + 15
$$

The eigenvalues of `C` are the roots of the characteristic polynomial:

$$
\lambda^2 - 8\lambda + 15 = 0 \Rightarrow (\lambda - 3)(\lambda - 5) = 0 \Rightarrow \lambda_1 = 3, \lambda_2 = 5
$$

The eigenvectors of `C` are given by solving the equation `(C - λI)v = 0` for each eigenvalue `λ`. For `λ_1 = 3`, we have:

$$
(C - \lambda_1 I)v_1 = \begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}v_1 = 0 \Rightarrow v_1 = t\begin{bmatrix}
-1 \\
1
\end{bmatrix}
$$

For `λ_2 = 5`, we have:

$$
(C - \lambda_2 I)v_2 = \begin{bmatrix}
-1 & 1 \\
1 & -1
\end{bmatrix}v_2 = 0 \Rightarrow v_2 = t\begin{bmatrix}
1 \\
1
\end{bmatrix}
$$

Thus, the eigenvectors of `C` are `v_1 = [-1, 1]` and `v_2 = [1, 1]`. We can normalize these eigenvectors to obtain an orthogonal matrix `Q`:

$$
Q = \frac{1}{\sqrt{2}}\begin{bmatrix}
-1 & 1 \\
1 & 1
\end{bmatrix}
$$

The diagonal matrix `Λ` is given by:

$$
Λ = \begin{bmatrix}
\lambda_1 & 0 \\
0 & \lambda_2
\end{bmatrix} = \begin{bmatrix}
3 & 0 \\
0 & 5
\end{bmatrix}
$$

Thus, we have decomposed `C` into the expression:

$$
C = QΛQ^T = \frac{1}{\sqrt{2}}\begin{bmatrix}
-1 & 1 \\
1 & 1
\end{bmatrix}\begin{bmatrix}
3 & 0 \\
0 & 5
\end{bmatrix}\left(\frac{1}{\sqrt{2}}\begin{bmatrix}
-1 & 1 \\
1 & 1
\end{bmatrix}\right)^T
$$


