# MA251-Algebra-I-Advanced-Linear-Algebra-Revision
My own notes about MA251, including example sheets and past papars

This repository will mainly focus on two parts, support class questions and past papers. I will provide the pdf made by myself so there will not be any problems about license.

## Lecture notes

[Lecture notes version 28.10.2022 (parts of section on quadratic forms rewritten).pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra/files/11111936/Lecture.notes.version.28.10.2022.parts.of.section.on.quadratic.forms.rewritten.pdf)

First thing first, lecture notes. Feel free to download the 2022 version from University of Warwick.

## Support Class Questions

The following theorems are taken from support classes in weekly order.

### Week 2

[MA251_Algebra_I_week_2.pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra/files/11111906/MA251_Algebra_I_week_2.pdf)

This week is basically a recap of what we learnt in first years. There are some theorem to bear in mind.

#### Span

* Given $n,m\in\mathbb{Z}^{+}$ and $n < m$, then $n$ vectors cannot span $\mathbb{R}^{m}$.

#### Rotational matrices

* For $2\times 2$ matrices, the anticlockwise rotation matrix of $\mathbb{R}^{2}$ is 

```math
\begin{bmatrix}\cos(\theta)& -\sin(\theta)\\ \sin(\theta) & \cos(\theta) \end{bmatrix}.
```

#### Matrix dimension

* Remember all the mapping matrices are multiplied to the left of the input vector, so based on the dimension of vector to determine the dimension of the matrix.

#### Change of basis

Given a linear map $T: V\to W$ and the ordered bases $\mathbf{E} = (e_{1},...,e_{n})$ and $\mathbf{F} = (f_{1},..., f_{m})$ of $V$ and $W$, we are asked to find the matrix of $T$ respect to the basis $\mathbf{E}'$ in $V$ and $\mathbf{F}'$ in $W$.

* The formula is given $$M(T)_{\mathbf{E}'}^{\mathbf{F}'}=M(\text{id}W)_F^{F'}\cdot M(T)_E^{F}\cdot M(\text{id}V)_E'^{E}.$$ Same as $$B = Q^{-1}AP.$$
* When computing the matrices, remember to find the reverse coefficients, i.e. When computing $M(\text{id}W)_F^{F'}$, though it is a map from $F\to F'$, we should use $$\mathbf{f}_1 = a\mathbf{f'}_1+b\mathbf{f'}_2$$ to find $a$ and $b$.

#### Transpose annd determinants

* Eigenvalues of a tranpose of a mtrix are equal.
* Determinants are equal to each other as well. $$\det(A) = \det(A^{t}).$$
* Determinant properties: $$\det(AB) = \det(A)\det(B),\quad \det(\alpha A) = \alpha^{n} A$$ where $n = \dim(A)$ and $\alpha\in\mathbb{R}$. 
