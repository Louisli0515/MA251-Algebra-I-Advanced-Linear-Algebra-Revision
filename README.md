# MA251-Algebra-I-Advanced-Linear-Algebra-Revision
My own notes about MA251, including example sheets and past papars

This repository will mainly focus on two parts, support class questions and past papers. I will provide the pdf made by myself so there will not be any problems about license.

- [MA251-Algebra-I-Advanced-Linear-Algebra-Revision](#ma251-algebra-i-advanced-linear-algebra-revision)
  * [Lecture notes](#lecture-notes)
  * [Support Class Questions](#support-class-questions)
    + [Week 2](#week-2)
      - [Span](#span)
      - [Rotational matrices](#rotational-matrices)
      - [Matrix dimension](#matrix-dimension)
      - [Change of basis](#change-of-basis)
      - [Transpose annd determinants](#transpose-annd-determinants)
    + [Week 3](#week-3)
      - [Characteristic polynomial and minimal polynomial](#characteristic-polynomial-and-minimal-polynomial)
      - [Eigenspace](#eigenspace)
      - [Diagonalisable](#diagonalisable)
      - [Something about $(J_{\lambda,n} - \lambda I_{n})^{r}$](#something-about---j---lambda-n-----lambda-i--n----r--)
      - [Direct Sum](#direct-sum)
      - [Alternative way to calculate $c_{A}(x)$ and $\mu_{A}(x)$](#alternative-way-to-calculate--c--a--x---and---mu--a--x--)
    + [Week 4](#week-4)
      - [Jordan basis](#jordan-basis)
      - [Compute JCF of a matrix $A$](#compute-jcf-of-a-matrix--a-)
    + [Week 5](#week-5)
      - [More about JCF](#more-about-jcf)
      - [Powers of matrix](#powers-of-matrix)
      - [Function of matrix](#function-of-matrix)
    + [Week 6](#week-6)
      - [Bilinear forms](#bilinear-forms)
      - [Quadratic forms](#quadratic-forms)
    + [Week 7](#week-7)
      - [Basis for quadratic forms](#basis-for-quadratic-forms)
      - [QR-decomposition](#qr-decomposition)
    + [Week 8](#week-8)
      - [Orthonormal basis](#orthonormal-basis)
      - [Different curves and surfaces](#different-curves-and-surfaces)
    + [Week 9](#week-9)
      - [SVD](#svd)
      - [Cosets](#cosets)
      - [Isomorphism](#isomorphism)
      - [Homomorphisms](#homomorphisms)
      - [Kernel](#kernel)
      - [The First Isomorphism Theorem](#the-first-isomorphism-theorem)
    + [Week 10](#week-10)
      - [Proposition about group homomorphism](#proposition-about-group-homomorphism)
      - [Corollary about group homomorphism](#corollary-about-group-homomorphism)
      - [Techniques when checking if it forms a basis.](#techniques-when-checking-if-it-forms-a-basis)
      - [Direct sum of abelian groups](#direct-sum-of-abelian-groups)
      - [Smith Normal Form](#smith-normal-form)




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

#### Powers of matrix

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

#### Function of matrix

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
* Given the degree is 2, we take the Lagrange interpolation of $z^{n}$ at the roots of $(z+2)^{2}$ to be $h(z) = \alpha z+ \beta.$
* To determine $\alpha$ and $\beta$, we solve $$f(\lambda) = h(\lambda) = -\alpha \lambda + \beta,$$ and $$f'(\lambda) = h'(\lambda) = \alpha.$$
* Therefore, $$f(A) = \alpha A+\beta I.$$

### Week 6

[MA251_Algebra_I_week_6.pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra-Revision/files/11130611/MA251_Algebra_I_week_6.pdf)

In week 6's support class, we focus more on quadratic forms and bilinear forms.

#### Bilinear forms 

* If given a quadratic form $\tau(x,y) = x_{1}y_{1}+x_{2}y_{2}+x_{3}y_{3}+x_{1}y_{3}$ for example, we first write its matrix where the rows representing the coefficient of $x_{i}$ (It is $y_{i}$ in this case) and columns representing the coefficient of $y_{i}$ (It is $x_{i}$ in this case).
* Now check the matrix is symmetric or not by checking if $A = A^{T}$.
* The ***left radical*** is defined as the kernel of $A^{T}$ and the ***right radical*** is defined as the kernel of $A$.
* If asked to write the matrix in the new basis, first write out the change of basis matrix by writing vertically of the new basis, and then use the formula $$B = P^{T}AP$$ to find the matrix in the new basis.
* To check if the matrix is non-degenerate or degenerate, check the rank of the matrix. If the rank of the matrix is ***full rank***, then it has no kernel and thus $\tau$ has zero right radical and it ***is non-degenerate***, otherwise it is ***not non-degenerate***.

#### Quadratic forms

* If given the quadratic forms $q_{1}(v) = -x^{2}+y^{2}$ for example, we first write its matrix, where (1,1)th entry represent the coefficient of $x^{2}$; (1,2)th entry represent the coefficient of $x$; (2,1)th entry represent the coefficient of $y$; (2,2)th entry represent the coefficient of $y^{2}$.
* The signature is determined by the number of positive and negative ***eigenvalues*** of the matrix above, written in pairs.

### Week 7

[MA251_Algebra_I_week_7.pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra-Revision/files/11130844/MA251_Algebra_I_week_7.pdf)

In week 7's support class, we focus on two parts: ***Basis for quadratic forms*** and ***QR-decomposition***.

#### Basis for quadratic forms

* Given a quadratic form, we can find a basis in which the matrix of the quadratic form is diagonal.
* ***First step***, check $a_{11}$ is 0 or not. If $a_{11} \ne 0$, then we are done in step 1; 
* If $a_{11}=0$, but $a_{ii}\ne 0$ for some $i > 1$, then we interchange $\mathbf{b}_1$ and $\mathbf{b}_i$;  
* If $a_{11}=0$ for all $i$, but there are some $i,j$ such that $a_{ij}\ne 0$, then we replace $\mathbf{b}_i$ with $\mathbf{b}_i+\mathbf{b}_j$;
* If $a_{ij}=0$ for all $i$ and $j$, then the matrix is $\mathbf{0}$, which is diagonal. 
* Write down the change of basis matrix $P$ in this step.

* ***Second step***, replace $\mathbf{b}_i$ with $\mathbf{b}_i- \frac{a1i}{a11}\mathbf{b}_1.$ and fix $\mathbf{b}'_1 = \mathbf{b}_1$.
* Now the change of basis matrix is 
```math
Q = \begin{bmatrix} 1 & -\frac{a12}{a11} & ... & -\frac{a1n}{a11}\\
0 & 1 & ... & 0\\
0 & 0 & ... & 0\\
0 & 0 & ... & 1 \end{bmatrix}.
```

* Combining the change of basis matrices, $$P' = PQ,$$ and the new matrix in this basis is $$B = (P')^{T}AP'.$$

* ***Third step***, if now $a_{11}\ne 0$, then we can focus on the smaller block $(n-1)\times(n-1)$ and repeat the previous steps.
* Note that in ***step 2***, $\mathbf{b}_i = \mathbf{b}_i - \frac{a2i}{a22}\mathbf{b}'_2$ and fix $\mathbf{b}''_1 = \mathbf{b}'_1$ and $\mathbf{b}''_2 = \mathbf{b}'_2$.
* The change of basis matrix is 
```math
Q' = \begin{bmatrix} 1 & 0 & ... & 0\\
0 & 1 & ... & -\frac{a2n}{a22}\\
0 & 0 & ... & 0\\
0 & 0 & ... & 1 \end{bmatrix}.
```

* Combining the change of basis matrices, $$P'' = P'Q',$$ and the new matrix in this basis is $$C = (P'')^{T}AP''.$$

#### QR-decomposition

* Grant-Schmidt process: Let $V$ be a euclidean space of dimension $n$ and suppose that, for some $r$ with $0\leq r\leq n$, $\mathbf{f}_1,...,\mathbf{f}_r$ are vectors in $V$ such that $$\mathbf{f}_i\cdot\mathbf{f}_j = \delta ij$$ for $1\leq i,j\leq r$.
* First check the determinant of a matrix is not 0.
* Let $\mathbf{g}_1, \mathbf{g}_2,...,\mathbf{g}_n$ be the columns of the matrix $A$. 
* ***First step***. Compute the first vector $\mathbf{f}_1$ by $$\mathbf{f}_1 = \frac{\mathbf{g}_1}{\left|\mathbf{g}_1\right|}.$$
* ***Second step***. Take $\mathbf{f}'_2 = \mathbf{g}_2 - (\mathbf{g}_2\cdot\mathbf{f}_1)\mathbf{f}_1$ and $$\mathbf{f}_2 = \frac{\mathbf{f}'_2}{\left|\mathbf{f}'_2\right|}.$$
* ***Third step***. Take $\mathbf{f}'_3 = \mathbf{g}_3 - (\mathbf{g}_3\cdot\mathbf{f}_1)\mathbf{f}_1 - (\mathbf{g}_3\cdot\mathbf{f}_2)\mathbf{f}_2$ and $$\mathbf{f}_3 = \frac{\mathbf{f}'_3}{\left|\mathbf{f}'_3\right|}.$$
* Continue the step and 
```math
Q = \begin{bmatrix} \mathbf{f}_1 & \mathbf{f}_2 & ... & \mathbf{f}_n \end{bmatrix}.
```
* Since we know $R$ is upper-triangular, we just have to write $R$ in that form and multiply by $Q$ and compare the coefficients or $Q$ is given by

```math
Q = \begin{bmatrix} \mathbf{f}_1\cdot\mathbf{g}_{1} & \mathbf{f}_1\cdot\mathbf{g}_{2} & ... & \mathbf{f}_{1}\cdot\mathbf{g}_{n}\\ 0 & \mathbf{f}_{2}\cdot\mathbf{g}_{2} & ... & \mathbf{f}_{2}\cdot \mathbf{g}_{n}\\ \vdots & \vdots & \ddots & \vdots \\0 & 0 & ... & \mathbf{f}_{n}\cdot\mathbf{g}_{n}\end{bmatrix}.
```

### Week 8

[MA251_Algebra_I_week_8.pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra-Revision/files/11136705/MA251_Algebra_I_week_8.pdf)


In week 8's support class, we focus on the following knowledge.

#### Orthonormal basis

* If we are asked to find an orthonormal basis in which the matrix is diagonal, the ***first step*** we should do is to find the characteristic polynomials.
* ***Second step***, we find the corresponding eigenvectors and make them length 1.
* ***Third  step***, check that if the dot product of the eigenvectors are 0.

#### Different curves and surfaces

* $n = 2$.

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/229383960-2a3544eb-b382-4b7d-92b6-b63e7f7fb421.png>

* $n = 3$.

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/229384150-19e52d0b-5ba1-4312-a7a6-626bda175776.png>
<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/229384152-39bbd54b-f955-49f9-ac14-ab2c43102635.png>
<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/229384158-1a135492-fdab-4a41-92ab-bd214de19f0e.png>
<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/229384159-1c2e35c0-ea11-4df8-be1c-300e4a579df7.png>
<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/229384161-afb3caf3-37ff-4263-9c34-0b61289af591.png>


### Week 9

[MA251_Algebra_I_week_9.pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra-Revision/files/11143031/MA251_Algebra_I_week_9.pdf)

In week 9's support class, we are moving on to groups.

#### SVD

* Given any real $k\times m$ matrix $A$, there exists unique singular values $\gamma_{1}\geq\gamma_{2}\geq...\geq\gamma_{n} > 0$ and orthogonal matrices $P$ and $Q$ such that 
```math
 \begin{bmatrix} D & 0\\
0  & 0
\end{bmatrix} = P^{T}AQ
```
where $D = \text{diag}(\gamma_{1},...,\gamma_{n})$.
* The steps of finding SVD follows from QR-decomposition but now $Q = P$ and $R = Q$ (all left symbols represent the ones in QR-decomposition); However, we should start with the matrix $A^{T}A$.

#### Cosets

Something about cosets should be remembered:

The following are equivalent for $g,k\in G$:

* $k\in H+g$
* $H+g = H+k$
* $k-g\in H$.

Also there are other lemmas and theorems about cosets.

* If $H$ is a subgroup of the abelian group $G$ and $H+g, H+k$ are cosets of $H$ in $G$, then $$(H+g)+(H+k) = H+(g+k).$$

#### Isomorphism

* A bijection $\phi:G\to H$ between two groups is called an isomorphism if $$\phi(g+h) = \phi(g)+\phi(h)$$ for all $g,h\in G$.

#### Homomorphisms

* Let $G$ and $H$ be groups. A homomorphism $\phi$ from $G$ to $H$ is a map $\phi:G\to H$ such that $$\phi(g_{1}+g_{2}) = \phi(g_{1})+\phi(g_{2})$$ for all $g_{1},g_{2}\in G$.

#### Kernel

* Let $\phi:G\to H$ be a homomorphism, then the kernel $\ker(\phi)$ of $\phi$ is defined to be the set of elements of $G$ that map onto $0_{H}$, that is $$\ker(\phi) = \set{g|g\in G, \phi(g) = 0_{H}}.$$ Note that $\ker(\phi)$ always contains $0_{G}$.
* Let $\phi:G\to H$ be a homomorphism. Then $\phi$ is injective if and only if $\ker(\phi) = \set{0_{G}}.$
* Let $\phi:G\to H$ be a group homomorphism with kernel $K$ and let $A$ be a subgroup of $G$. Then induced map $\bar{\phi}:G/A\to H$ via $\bar{\phi}(A+g) = \phi(g)$ for all $g\in G$ is a group homomorphism if and only if $A\leq K$.

#### The First Isomorphism Theorem

* Let $\phi:G\to H$ be a homomorphism with kernel $K$. Then $G/K\cong\text{im}(\phi).$ More precisely, there is an isomorphism $\bar{\phi}:G/K\to\text{im}(\phi)$ defined by $$\bar{\phi}(K+g) = \phi(g)$$ for all $g\in G$.

### Week 10

[MA251_Algebra_I_week_10.pdf](https://github.com/Louisli0515/MA251-Algebra-I-Advanced-Linear-Algebra-Revision/files/11159645/MA251_Algebra_I_week_10.pdf)


In week 10's support class, we focus more on quotient groups and cyclic groups.


#### Proposition about group homomorphism

Consider elements $g_{1},...,g_{n}$ of an abelian group $G$. It is possible to extend this assignment $\phi(x_i) = g_{i}$ to a group homomorphism $\phi:\mathbb{Z}^{n}\to G$. We define $\phi((a_{1},a_{2},...,a_{n})^{T}) = \displaystyle\sum_{i=1}^{n}a_{i}g_{i}$, then 

* The function $\phi$ is a group homomorphism.
* The set of elements $\set{g_{i}}$ are linearly independent if and only if $\phi$ is injective.
* The set of elements $\set{g_{i}}$ span $G$ if and only if $\phi$ is surjective.
* The set of elements $\set{g_{i}}$ form a free basis of $G$ if and only if $\phi$ is an isomorphism.

#### Corollary about group homomorphism

Let $G$ be a free abelian group with a free basis $g_{1},...,g_{n}$. Let $H$ be an abelian group and $a_{1},...,a_{n}\in H$. Then there exists a unique group homomorphism $\phi:G\to H$ such that $$\phi(g_{i}) = a_{i}$$ for all $i$.

#### Techniques when checking if it forms a basis.

* Given $n$ vectors, and we want to check if they form a basis in $\mathbb{R}^{n}$. The old-fashion way is to check their linear independence and span. 
* Another way is write them in columns 
```math
A = \begin{bmatrix} \mathbf{v}_{1}&...&\mathbf{v}_{n} \end{bmatrix}.
```
Then we find its determinant to see if it is 1, if it is 1, then its columns form a basis in $\mathbb{R}^{n}$.

* If the determinant of it is non-zero, then immediately we can conclude the vectors are linearly independent.

#### Direct sum of abelian groups

* The direct sum of a finite number of abelian groups is the same as their cartesian product, just with different notation. For example, try writing out all the 15 elements of $\mathbb{Z}/3\mathbb{Z}\oplus\mathbb{Z}/5\mathbb{Z}$.
* They will look like $a\oplus b$ where $a$ is an integer mod 3 and $b$ is an integer mod 5. Therefore, for example $$(2\oplus 3)+(1\oplus 4) = ((2+1)\mod 3)\oplus((3+4)\mod 5) = 0\oplus 2.$$
* The identity element will be $0\oplus 0$. 
* The inverse of $(2\oplus 3)$ will be $$-(2\oplus 3) = (-2\mod 3\oplus-3\mod 5) = 1\oplus 2.$$
* Any subgroup of prime order would be ***isomorphic*** to a cyclic group of its order.
* Let $G = G_{1}\oplus G_{2}\oplus...\oplus G_{n}$ be a finite abelian group. The order of $g = (g_{1},g_{2},...,g_{n})$ is the least common multiple of the orders $|g_{i}|$ of the components of $g$.

#### Smith Normal Form

* Let $A$ be an $m\times n$ matrix over $\mathbb{Z}$ with rank $r$. The uniquely determined diagonal matrix, where $d_{i}$ satisfy $d_{i}>0$ for $1\leq i\leq r$ and $d_{i}\vert d_{i+1}$ for $1\leq i < r$ is called the unimodular Smith normal form of $A$.

How to find the SNF of a matrix?

* ***Step 1***: Find $d_{1}$, which is the greatest common divisor of all the entries of $A$.
* ***Step 2***: If $d_{1}$ occurs as an entry in $A$ move it to the (1,1)th entry using column and row operations. 
* If $d_{1}$ does not occur, let $x$ be the smallest entry occuring in $A$, say in position $(i,j)$. Does $x$ divide everything else in the $i$ th row and $j$ th column? If not, let $y$ be an entry that $x$ does not divide, in position $(k,l)$ with $k=i$ or $l=j$. Then $y=sx+r$ with $r < x$ and using column and row operations, we can obtain $r=y-sx$ as an entry of $A$.
* If $x$ divides everything else in row $i$ and columns $j$. We start by clearing all of these entries to 0.
* ***Step 3***: With $d_{1}$ in the (1,1)th entry, we can use it to clear everything else in the first row and column since $d_{1}$ divides all entries in the matrix.
* ***Step 4***: We now go back to ***Step 1***, working on the $(m-1)\times(n-1)$ matrix in the bottom right hand corner. Repeating this process will terminate and will yield the SNF of $A$.
