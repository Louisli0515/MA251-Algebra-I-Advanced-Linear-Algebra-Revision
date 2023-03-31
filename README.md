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

### Week 3

[MA251_Algebra_I_week_3.pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra-Revision/files/11120383/MA251_Algebra_I_week_3.pdf)

In week 3's support class, there are some definitions and theorems we should bear in mind.

#### Characteristic polynomial and minimal polynomial

* Definition for Characteristic polynomial: $$c_{A}(x) = \det(A-xI_{n})$$ where $n = \dim(A)$. 
* Definition for Minimal polynomial: $$\mu_{A}(x) = 0$$ with the least degree and monic.
* By Cayley Hamilton Theorem, $$\mu_{A}(x)\vert c_{A}(x).$$

#### Eigenspace

* If the question asks you to find the generalised eigenspace of a matrix $A$ of eigenvalue $\lambda$, then it means to find the nullspace of it, meaning to find all $\mathbf{v}$ s such that $$(A-\lambda I_{n})^{r}\mathbf{v} = 0,$$ where $r$ is determined by the eigenspace's dimension.

#### Diagonalisable

* A matrix $A$ is diagonalisable if and only if has a basis of eigenvectors.
* Sometimes when we compute all the generalised eigenvectors and want to determine if the matrix is diagonlisable or not, we need to check if they are all eigenvectors of the matrix, i.e. Check if $$A\mathbf{v} = \lambda \mathbf{v}.$$ If there are less number of eigenvectors than the dimension of the matrix, then it cannot form a basis of eigenvectors and hence the matrix $A$ is not diagonlisable.

#### Something about $(J_{\lambda,n} - \lambda I_{n})^{r}$

* Note that $(J_{\lambda,n} - \lambda I_{n})^{r}$ is shown in the result like follows:
```math
\begin{bmatrix}0&1&0&0&0&...\\ 0 & 0&1&0&0&...\\ 0&0&0&1&0&...\\ \vdots&\vdots&\vdots&\vdots&\vdots \end{bmatrix}^{r}.
```

This is nothing but we move the diagonal line of 1 upward by one place.

* In particular, $(J_{\lambda,n} - \lambda I_{n})^{n-1}$ is a matrix with all zeros apart from the $1,n$ entry, which is a 1.

#### Direct Sum

* Remember some properties: $$\det(A\oplus B) = \det(A)\det(B),$$ and $$\mu_{A\oplus B}(A\oplus B) = \mu_{A\oplus B}(A)\oplus \mu_{A\oplus B}(B). $$
* Let $M = A\oplus B$, then $$c_{M}(x) = c_{A}(x)c_{B}(x)$$ and $$\mu_{M}(x) = lcm(\mu_{A}(x), \mu_{B}(x)).$$

#### Alternative way to calculate $c_{A}(x)$ and $\mu_{A}(x)$

* Theorem 2.7.4 in the notes says $$c_{A}(x) = (-1)^{n}\prod_{i=1}^{r}(x-\lambda_{i})^{a_{i}},$$ where $a_{i}$ is the sum of the degrees of Jordan blocks of $A$ of eigenvalue $\lambda_{i}$ and $$\mu_{A}(x) = \prod_{i=1}^{r}(x-\lambda_{i})^{b_{i}},$$ where $b_{i}$ is the largest among the degrees of Jordan blocks of $A$ of eigenvalue $\lambda_{i}$.

### Week 4

[MA251_Algebra_I_week_4.pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra-Revision/files/11122508/MA251_Algebra_I_week_4.pdf)

In week 4's support class, we should focus on the algorithms and theorems of JCF.

#### Jordan basis

* The algorithm of finding Jordan basis is to find the value of r such that $$(A-\lambda I_{n})^{r} = 0.$$ 
* Then, choose a random vector $\mathbf{v}$ such that $$\mathbf{v}\in{\ker(A-\lambda I_{n})^{r}}\setminus{\ker(A-\lambda I_{n})^{r-1}},$$ i.e. choose $\mathbf{v}$ such that $$(A-\lambda I_{n})^{r}= 0\quad\text{and}\quad (A-\lambda I_{n})^{r-1}\ne 0.$$
* After that, compute the second $\mathbf{v}'$ using $$\mathbf{v}' = (A-\lambda I_{n})\mathbf{v}.$$
* Continute the above process till the final vector.

#### Compute JCF of a matrix $A$

There are two ways of doing it.

* ***Brutal force***: By calculating the characteristic polynomial $c_{A}(x)$ and Cayley Hamilton Theorem, we can find the minimal polynomial $\mu_{A}(x)$.
* By Theorem 2.7.4, we know the power of $c_{A}(x)$ is the sum of sizes of Jordan blocks and the power of $\mu_{A}(x)$ is the largest size of the Jordan block.

* ***Nullity method***: By Theorem 2.9.1, we know that for $i > 0$, the number of Jordan blocks of $J$ with eigenvalue $\lambda$ and degree at least $i$ is equal to nullity $((A-\lambda I_{n})^{i})$ - nullity $((A-\lambda I_{n})^{i-1})$.
* Theorem 2.9.1 also states that the number of Jordan blocks of $J$ with eigenvalue $\lambda$ is equal to the nullity $(A-\lambda I_{n})$.
* Again by Theorem 2.7.4, the power of $c_{A}(x)$ is the sum of sizes of Jordan blocks and the power of $\mu_{A}(x)$ is the largest size of the Jordan block.
* Compare these two theorems, we can know the combination of Jordan blocks with each eigenvalue.

### Week 5

[MA251_Algebra_I_week_5 .pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra-Revision/files/11127575/MA251_Algebra_I_week_5.pdf)

In week 5's support class, we are still focusing on some algorithms.

#### More about JCF

* Last week we learnt how to compute JCF of a matrix $A$. However sometimes the question asks to find a matrix $P$ such that $$P^{-1}AP = J.$$
* We first find the Jordan basis of $A$. Note here that if $\dim(A) > \text{number of vectors}$, we first need to choose two random eigenvectors which are linearly independent, namely $\mathbf{v}_2$ and $\mathbf{v}_4$. (Assume $\dim(A) = 4$ and we only have one eigenvalue)
* Be careful here the Jordan chain is computed reversely, so $$\mathbf{v}_1=(A-\lambda I_4)\mathbf{v}_2$$ and $$\mathbf{v}_3=(A-\lambda I_4)\mathbf{v}_4.$$ Check that $\mathbf{v}_1$ and $\mathbf{v}_3$ are linearly independent.
* Then 
```math
P = \begin{bmatrix} \mathbf{v}_1 & \mathbf{v}_2 & \mathbf{v}_3 & \mathbf{v}_4 \end{bmatrix}.
```

### Powers of matrix

There are two methods to compute it.
* ***Direct Calculation***
* If $J = P^{-1}AP$ is the JCF of $A$ then it is sufficient to compute $J^{n}$ because of the telescoping product $$A^{n} = (PJP^{-1})^{n} = PJ^{n}P^{-1}.$$
* Note that $$(B\oplus C)^{n} = B^{n}\oplus C^{n}.$$
* By induction, 

```math
J_{\lambda,k}^{n} = \begin{bmatrix} \lambda^{n} & n\lambda^{n-1} & ... & C_{k-1}^{n}\lambda^{n-k+1}\\
0 & \lambda^{n} & ... & C_{k-2}^{n}\lambda^{n-k+2}\\
\vdots & \vdots & \vdots & \vdots\\
0 & 0 & ... & \lambda^{n}\end{bmatrix}.
```

* ***Lagrange's Interpolation***
* Find the minimal polynomial $\mu_{A}(x)$ first, here suppose $\mu_{A}(z) = (z+2)^{2}.$
* Given the degree of $\mu_{A}(x)$ is 2, we take the Lagrange interpolation of $z^{n}$ at the roots of $(z+2)^{2}$ to be $h(z) = \alpha z + \beta.$
* To determine $\alpha$ and $\beta$, we need to solve $$(\lambda)^n = h(\lambda) = -\alpha \lambda + \beta,$$ and $$n(\lambda)^{n-1} = h'(\lambda) = \alpha.$$
* Therefore, $$A^{n} = \alpha A+\beta I.$$

### Function of matrix

Similarly, it has two methods.

* ***Direct Calculation***

* Let $J = P^{-1}AP$ with $J$ being the JCF of $A$, then $$f(A) = Pf(J)P^{-1}.$$ and 

```math
f(J_{\lambda,k}) = \begin{bmatrix} f(\lambda) & f'(\lambda) & ... & f^{[k-1]}(\lambda)\\
0 & f(\lambda) & ... & f^{[k-2]}(\lambda)\\
\vdots & \vdots & \vdots & \vdots\\
0 & 0 & ... & f(\lambda)\end{bmatrix},
```
where $$f^{[k]}(z) = \frac{1}{k!}f^{(k)}(z).$$

* ***Lagrange's Interpolation***
* Find the minimal polynomial $\mu_{A}(x)$ first, here suppose again $\mu_{A}(x) = (z+2)^{2}.$
* Given the degree is 2, we take the Lagrangfe interpolation of $z^{n}$ at the roots of $(z+2)^{2}$ to be $h(z) = \alpha z+ \beta.$
* To determine $\alpha$ and $\beta$, we solve $$f(\lambda) = h(\lambda) = -\alpha \lambda + \beta,$$ and $$f'(\lambda) = h'(\lambda) = \alpha.$$
* Therefore, $$f(A) = \alpha A+\beta I.$$
