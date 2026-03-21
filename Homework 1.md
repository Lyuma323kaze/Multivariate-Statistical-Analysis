
### Prob. 1

By definition, 
$$
\begin{gathered}
\boldsymbol{\mu} = {1\over 2} \left(
\begin{bmatrix} 
3 \\ 4 \\ 5 \\ 4 \\ 
\end{bmatrix} + \begin{bmatrix}
6 \\ 4 \\ 7 \\ 7
\end{bmatrix}
\right) = \begin{bmatrix}
4.5 \\ 4 \\ 6 \\ 5.5
\end{bmatrix}
\end{gathered}
$$
When it comes to covariance matrix $\Sigma$ :
$$
\begin{align*}
\boldsymbol{X}_{1} =& \begin{bmatrix} 
3 \\ 4 \\ 5 \\ 4 \\ 
\end{bmatrix}
,
\boldsymbol{X}_{2} = \begin{bmatrix}
6 \\ 4 \\ 7 \\ 7
\end{bmatrix}
\\
\boldsymbol{\Sigma} =& \sum^{2}_{i=1} (\boldsymbol{X}_{i} - \boldsymbol{\mu})(\boldsymbol{X}_{i} - \boldsymbol{\mu})'\\
=& 2\times \begin{bmatrix}
2.25 & 0 & 1.5 & 2.25\\
0 & 0 & 0 & 0 \\
1.5 & 0 & 1 & 1.5\\
2.25 & 0 & 1.5 & 2.25
\end{bmatrix}\\
=& \begin{bmatrix}
5 & 0 & 3 & 5\\
0 & 0 & 0 & 0 \\
3 & 0 & 2 & 3\\
5 & 0 & 3 & 5
\end{bmatrix}
\end{align*}
$$

### Prob. 2
#### (a)
We know that
$$
\boldsymbol{X} = \begin{bmatrix}X_{1} \\ X_{2} \\ X_{3}\end{bmatrix}
$$
Therefore, the target expression could be expressed as
$$
\begin{align*}
Z =& 3X_{1} - 2X_{2} + X_{3}\\
=& \begin{bmatrix}3 & -2 & 1\end{bmatrix}\begin{bmatrix}
X_{1}\\
X_{2}\\
X_3
\end{bmatrix}\\
=& A \boldsymbol{X}
\end{align*}
$$
where
$$
A = \begin{bmatrix}3 & -2 & 1\end{bmatrix}
$$
So that we can obtain that
$$
\begin{align*}
\boldsymbol{\mu}_{Z} =& A \boldsymbol{\mu}\\
=& \begin{bmatrix}3 & -2 & 1\end{bmatrix}\begin{bmatrix}
2\\
-3 \\
1
\end{bmatrix}\\
=& 1\\
\Sigma_{Z} =& A \boldsymbol{\Sigma}A'\\
=& \begin{bmatrix}3 & -2 & 1\end{bmatrix} \begin{bmatrix}
1 & 1 & 1\\
1 & 3 & 2\\
1 & 2 & 2
\end{bmatrix}\begin{bmatrix}3 \\
 -2 \\
 1\end{bmatrix}\\
=& 9
\end{align*}
$$
#### (b)
Define a novel  random variable $Y$:
$$
Y = \begin{bmatrix}X_{2} \\ X_{1} \\ X_{3} \end{bmatrix}
$$
Then the problem is converted to:
Find a $2\times 1$ vector $\boldsymbol{a}$ such that for matrix $A$ and random variable $\boldsymbol{Z}$ defined as below:
$$
\begin{gathered}
A = \begin{bmatrix}
1 & 0 & 0 \\ 
1 & -\boldsymbol{a}'
\end{bmatrix} = \begin{bmatrix}
1 & 0 & 0 \\ 
1 & -a_{1} & -a_{2}
\end{bmatrix}
\\
Z = A \boldsymbol{Y} = \begin{bmatrix}
X_{2} \\ X_{2} - \boldsymbol{a}'\begin{bmatrix}X_{1} \\ X_{3}\end{bmatrix} 
\end{bmatrix}
\end{gathered}
$$
the covariance matrix of $Z$ , $\Sigma_{Z}$, should be diagonal.
The covariance matrix of $Y$ should be expressed as
$$
\Sigma_{Y}= \begin{bmatrix}
3 & 1 & 2 \\ 1 & 1 & 1 \\ 2 & 1 & 2
\end{bmatrix}
$$
$\Sigma_{Z}$ could be calculated as
$$
\begin{align*}
\Sigma_{Z} =& A \Sigma_{Y} A'\\
=& \begin{bmatrix}
1 & 0 & 0 \\ 
1 & -a_{1} & -a_{2}
\end{bmatrix} \begin{bmatrix}
3 & 1 & 2 \\ 1 & 1 & 1 \\ 2 & 1 & 2
\end{bmatrix}\begin{bmatrix}
1 & 1\\
0 & -a_{1}\\
0 & -a_{2}
\end{bmatrix}\\
=&\begin{bmatrix}
3 & 3-a_{1}-2a_{2}\\
3-a_{1}-2a_{2} & a_{1}^{2} + 2a_{1}a_{2}+2a_{2}^{2}-2a_{1}-4a_{2}+3
\end{bmatrix}
\end{align*}
$$
when $\Sigma_{Z}$ is diagonal, we find that $\boldsymbol{a}$ satisfies:
$$
\begin{gathered}
3 - a_{1} - 2a_{2} = 0
\end{gathered}
$$
A possible solution is
$$
\boldsymbol{a} = \begin{bmatrix}
1 \\ 1
\end{bmatrix}
$$

### Prob. 3
#### (1)
By definition, the distribution of $(X_{2},Y_{1})$ is still binormal. The mean value and covariance matrix:
$$
\begin{gathered}
\mu = \begin{bmatrix}2 \\ 1\end{bmatrix}
\\
\Sigma = \begin{bmatrix}2 & 0 \\ 0 &  3\end{bmatrix}
\end{gathered}
$$
#### (2)
The distribution for $Y_{2}|Y_{1}=y$ is normal, and the mean and covariance:
$$
\begin{gathered}
\mu = 3 + 3 \times {1\over7} \times (y-1)\\
\Sigma = 7- 3\times {1\over 3} \times 3 = 4
\end{gathered}
$$
#### (3)
The mean value is linear, therefore is evident that
$$
\boldsymbol{\mu_{W}} = \boldsymbol{\mu_{X}} - \boldsymbol{\mu_{Y}} = \begin{bmatrix}0 \\ -1\end{bmatrix}
$$
By defining the matrix $A$:
$$
A = \begin{bmatrix}
I_{2\times2} & 0 \\ 0  & I_{2\times2}
\end{bmatrix}
$$
we have
$$
\boldsymbol{W} = A\begin{bmatrix}\boldsymbol{X} \\ \boldsymbol{Y}\end{bmatrix}
$$
Hence, the covariance
$$
\Sigma_{W} = A\begin{bmatrix}
2 & 1 & 0 &0 \\ 1 & 2  & 0  & 0 \\ 0 &  0  & 3  & 3 \\ 0 &  0 & 3 & 7
\end{bmatrix}A' = \begin{bmatrix}
2 & 1 & 0 &0 \\ 1 & 2  & 0  & 0 \\ 0 &  0  & 3  & 3 \\ 0 &  0 & 3 & 7
\end{bmatrix}
$$

### Prob. 4
In the summation notation, we could easily find that
$$
\overline{\boldsymbol{x}} - \boldsymbol{\mu} = \boldsymbol{const}
$$
under summation. Therefore, the first summation is equivalent to
$$
\begin{align*}
\sum_{j=1}^{n}(\boldsymbol{x}_{j}-\overline{\boldsymbol{x}})(\overline{\boldsymbol{x}} - \boldsymbol{\mu})' =&  \left[
 \sum_{j=1}^{n}(\boldsymbol{x}_{j}-\overline{\boldsymbol{x}})
\right](\overline{\boldsymbol{x}} - \boldsymbol{\mu})'\\
=& \left[
\sum_{j=1}^{n} \boldsymbol{x}_{j} - n\times {1\over n}\sum_{j=1}^{n} \boldsymbol{x}_{j}
\right](\overline{\boldsymbol{x}} - \boldsymbol{\mu})'\\
=& \boldsymbol{0}(\overline{\boldsymbol{x}} - \boldsymbol{\mu})' = \boldsymbol{0}_{p\times p}
\end{align*}
$$
The dimension is given by the vectors themselves. Similarly, we can prove that 
$$
\begin{align*}
\sum_{j=1}^{n}(\overline{\boldsymbol{x}} - \boldsymbol{\mu})(\boldsymbol{x}_{j}-\overline{\boldsymbol{x}})' =&  (\overline{\boldsymbol{x}} - \boldsymbol{\mu})\left[
 \sum_{j=1}^{n}(\boldsymbol{x}_{j}-\overline{\boldsymbol{x}})
\right]'\\
=& (\overline{\boldsymbol{x}} - \boldsymbol{\mu})\boldsymbol{0}' = \boldsymbol{0}_{p\times p}
\end{align*}
$$

### Prob. 5
#### (1)
Suppose that ${\rm Cov}(\overline{\boldsymbol{X}}) = (\sigma_{ik}')_{p\times p},{\rm Cov}(\boldsymbol{X}) = (\sigma_{ik})_{p\times p}$, wthen
$$
\begin{align*}
\sigma_{ik}' =& {1\over n^{2}} E \left[
\left(
\sum_{j=1}^{n}x_{j,i} - \overline{\sum_{j=1}^{n}x_{j,i}}
\right) \left(
 \sum_{l=1}^{n}x_{l,k} - \overline{\sum_{l=1}^{n}x_{l,k}}
\right)
\right]\\
=& {1\over n^{2}}E \left[
\left(
\sum_{j=1}^{n}(x_{j,i} - \overline{x_{i}})
\right) \left(
 \sum_{l=1}^{n}(x_{l,k} - \overline{x_{k}})
\right)
\right]\\
=& {1\over n^{2}}\sum_{j=1}^{n}\sum_{l=1}^{n}E \left[
\left(
x_{j,i} - \overline{x_{i}}
\right) \left(
x_{l,k} - \overline{x_{k}}
\right)
\right]
\end{align*}
$$
Since all the samples are independent, therefore
$$
\begin{align*}
\sigma_{ik}' =& {1\over n^{2}}\sum_{j=1}^{n}\sum_{l=1}^{n}E \left[
\left(
x_{j,i} - \overline{x_{i}}
\right) \left(
x_{l,k} - \overline{x_{k}}
\right)
\right]\\
=& {1\over n^{2}}\sum_{j=1}^{n}\sum_{l=1}^{n}E \left[
\left(
x_{j,i} - \overline{x_{i}}
\right) \left(
x_{l,k} - \overline{x_{k}}
\right)
\right]\delta_{il}\\
=& {1\over n^{2}}\sum_{j=1}^{n}E \left[
\left(
x_{j,i} - \overline{x_{i}}
\right) \left(
x_{j,k} - \overline{x_{k}}
\right)
\right]\\
=& {1\over n^{2}}\cdot n \sigma_{ik}\\
=& {1\over n} \sigma_{ik}
\end{align*}
$$
Hence, 
$$
{\rm Cov}(\overline{\boldsymbol{X}}) = {1\over n} {\rm Cov}(\boldsymbol{X})
$$
#### (2)
The component expression of $\boldsymbol{S}$ :
$$
s_{ik} = {1\over n-1} \sum_{j=1}^{n}(X_{ji} - \overline{X_{i}})(X_{jk}-\overline{X_{k}})
$$
For $\boldsymbol{b}'\boldsymbol{X} = \sum_{i=1}^{p}b_{i}X_{i}$, the sample variance should be
$$
\begin{align*}
\sigma =& {1\over n-1}\sum_{j=1}^{n}\left(
\sum_{i=1}^{p}X_{ji}b_{i} - \sum_{i=1}^{p}\overline{X_{i}}b_{i} 
\right)\left(
\sum_{k=1}^{p}X_{jk}b_{k} - \sum_{k=1}^{p}\overline{X_{k}}b_{k} 
\right)\\
=& \sum_{i=1}^{p}\sum_{j=1}^{p}{1\over n-1} \sum_{j=1}^{n}(X_{ji} - \overline{X_{i}})(X_{jk}-\overline{X_{k}})b_{i}b_{k}\\
=& \sum_{i=1}^{p}\sum_{j=1}^{p}b_{i}b_{k}s_{ik}\\
\implies \boldsymbol{S}_{\boldsymbol{b'}\boldsymbol{X}} =& \boldsymbol{b}'\boldsymbol{S}\boldsymbol{b}
\end{align*}
$$

### Prob. 6
For clarification, we define
$$
\boldsymbol{\varepsilon} = \boldsymbol{X}_{1}- A \boldsymbol{X}_2
$$
And then we find that
$$
\boldsymbol{\varepsilon}|\boldsymbol{X}_{2}=x_{2}\sim N(Ax_{2}-Ax_{2},\boldsymbol{\Sigma_{11}})
$$
which is independent of $x_{2}$, therefore, $\boldsymbol{\varepsilon}$ is independent of $\boldsymbol{X}_{2}$.
Moreover, since both $\boldsymbol{\varepsilon}$ and $\boldsymbol{X_{2}}$ are multivariate normal, then 
$$
\begin{bmatrix}
\boldsymbol{\varepsilon} \\ \boldsymbol{X_{2}}
\end{bmatrix}
$$
is also multivariate normal. And by definition, 
$$
\begin{bmatrix}
\boldsymbol{X_{1}} \\ \boldsymbol{X_{2}}
\end{bmatrix} = \begin{bmatrix}
A \boldsymbol{X_{2}}+\boldsymbol{\varepsilon} \\ \boldsymbol{X_{2}}
\end{bmatrix}=\begin{bmatrix} 
\boldsymbol{I} & A \\ \boldsymbol{0} & \boldsymbol{I}
\end{bmatrix}\begin{bmatrix}
\boldsymbol{\varepsilon} \\ \boldsymbol{X_{2}}
\end{bmatrix} = M \begin{bmatrix}
\boldsymbol{\varepsilon} \\ \boldsymbol{X_{2}}
\end{bmatrix} 
$$
Therefore, 
$$
\begin{bmatrix}
\boldsymbol{X_{1}} \\ \boldsymbol{X_{2}}
\end{bmatrix}
$$
is multivariate normal. So that we can find that
$$
\begin{align*}
\boldsymbol{\mu} =& M\begin{bmatrix} 0 \\ \boldsymbol{\mu_{2}}\end{bmatrix} = \begin{bmatrix}A \boldsymbol{\mu_{2}} \\ A \boldsymbol{\mu_{2}}\end{bmatrix}
\\
\boldsymbol{\Sigma} =&  \begin{bmatrix} 
\boldsymbol{I} & A \\ \boldsymbol{0} & \boldsymbol{I}
\end{bmatrix}\begin{bmatrix}
\boldsymbol{\Sigma_{11}} & \boldsymbol{0}\\
\boldsymbol{0} & \boldsymbol{\Sigma_{22}}
\end{bmatrix}\begin{bmatrix} 
\boldsymbol{I} & \boldsymbol{0} \\ A & \boldsymbol{I}
\end{bmatrix}\\
=& \begin{bmatrix}
\boldsymbol{\Sigma_{11}} + A \boldsymbol{\Sigma_{22}}A' & A \boldsymbol{\Sigma_{22}}\\
\boldsymbol{\Sigma_{22}}A' & \boldsymbol{\Sigma_{22}}
\end{bmatrix}
\end{align*}
$$
and therefore
$$
\boldsymbol{X_{1}} \sim N(A \boldsymbol{\mu_{2}}, \boldsymbol{\Sigma_{11}} + A \boldsymbol{\Sigma_{22}}A' )
$$
### Prob. 7
By definition
$$
d(X, \mu)^{2} = (X-\mu) \Sigma^{-1} (X-\mu)
$$
therefore
$$
\begin{align*}
d(X,Y)^{2} =& (X-Y)'\Sigma(X-Y)\\
=& (X-\mu - (Y-\mu))' \Sigma^{-1} (X-\mu - (Y-\mu))\\
=& d(X,\mu)^{2}+d(Y,\mu)^{2}-2(X-\mu)'\Sigma^{-1}(Y-\mu)\\
=&2p -2E [(X-\mu)'\Sigma^{-1}(Y-\mu)]\\
=&2p -2E [(X-\mu)']\Sigma^{-1} E[(Y-\mu)]\\
=& 2p
\end{align*}
$$