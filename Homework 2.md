### Prob. 1
#### (1)
The quantity
$$
\begin{align*}
&(\boldsymbol{X}_{1} - \boldsymbol{\mu})'\Sigma^{-1}(\boldsymbol{X}_1-\boldsymbol{\mu})\\
=& [\Sigma^{-1\over 2}(\boldsymbol{X}_{1}-\boldsymbol{\mu})]'[\Sigma^{-1\over 2}(\boldsymbol{X}_{1}-\boldsymbol{\mu})]
\end{align*}
$$
has distribution for the parts
$$
\Sigma^{-1\over 2}(\boldsymbol{X}_{1}-\boldsymbol{\mu})\sim {\mathcal{N}} (0,I)
$$
therefore
$$
(\boldsymbol{X}_{1} - \boldsymbol{\mu})'\Sigma^{-1}(\boldsymbol{X}_1-\boldsymbol{\mu})\sim W_{3}(1, I)
$$
#### (2)
It's clear that
$$
\begin{gathered}
\overline{\boldsymbol{X}} = {1\over4}\sum_{i=1}^{4}\boldsymbol{X}_{i}\sim \mathcal{N}(\boldsymbol{\mu},\Sigma/4)
\\
\sqrt{n}(\overline{\boldsymbol{X}}-\boldsymbol{\mu})\sim \mathcal{N}(0, \Sigma)
\end{gathered}
$$
where
$$
{1\over4}\Sigma = \begin{bmatrix}
3/4 & -1/4 & 1/4 \\ -1/4 & 1/4 & 0 \\ 1/4 & 0 & 1/2
\end{bmatrix}
$$
#### (3)
We know that
$$
\boldsymbol{S}\sim {1\over n-1} W_{3}(n-1,\Sigma)
$$
For our case, $n=4$, therefore
$$
(n-1)\boldsymbol{S} \sim W_{3}(3,\Sigma)
$$
#### (4)
By the definition of sample variance, it's easy to find
$$
BSB'\sim W_{3}(3, B \Sigma B')
$$
and 
$$
\begin{align*}
B \Sigma B' =& \begin{bmatrix}
1 & 0 & 0\\
0 & 0 & 1
\end{bmatrix}\begin{bmatrix}
3 & -1 & 1\\
-1 & 1 & 0\\
1 & 0 & 2
\end{bmatrix}\begin{bmatrix}
1 & 0\\
0 & 0\\
0 & 1
\end{bmatrix}\\
=& \begin{bmatrix}
3 & 1\\
1 & 2
\end{bmatrix}
\end{align*}
$$
#### (5)
For the first linear combination, 
$$
\Sigma_{1} = 4\times {1\over 2^{2}} \Sigma = \Sigma
$$
For the second,
$$
\Sigma_{2} = (1+1+1+3^{2})\Sigma = 12\Sigma
$$
The covariance
$$
\begin{align*}
{\rm Cov} \left({1\over 2}\sum_{i=1}^{4}\boldsymbol{X}_{i}, \boldsymbol{X}_{1}+\boldsymbol{X}_{2}+\boldsymbol{X}_{3}-3\boldsymbol{X_{3}}\right)=& (3\times 2\times 1 - 3\times {1\over 2}){\rm Var}(\boldsymbol{X})\\
=& 0
\end{align*}
$$
### Prob. 2
#### (a)
The sample mean
$$
\overline{\boldsymbol{X}}=\begin{bmatrix}6 \\ 10\end{bmatrix}
$$
sample variance
$$
\begin{align*}
S =& {1\over 4}\sum_{i=1}^{4}(\boldsymbol{X_{i}}-\boldsymbol{\overline{X}})(\boldsymbol{X_{i}}-\boldsymbol{\overline{X}})'\\
=& \begin{bmatrix}8 & -10/3\\
-10/3 & 2\end{bmatrix}
\end{align*}
$$
The mean difference
$$
\overline{\boldsymbol{X}}-\boldsymbol{\mu} = \begin{bmatrix}-1 \\ -1\end{bmatrix}
$$
For the inverse of sample variance
$$
\begin{align*}
\det(S) =& {44\over9}\\
S^{-1}=& {S^{*}\over |S|} \\
=& {9\over 44}\begin{bmatrix}
2 & 10/3\\
10/3 & 8
\end{bmatrix}\\
=& \begin{bmatrix}
9/22 & 15/22\\
15/22 & 18/11
\end{bmatrix}
\end{align*}
$$
Hotelling's $T^{2}$
$$
T^{2} = n(\overline{\boldsymbol{X}}-\boldsymbol{\mu})'S^{-1}(\overline{\boldsymbol{X}}-\boldsymbol{\mu})
$$
Substituting $n=4$ and other data, we finally get
$$
T^{2}= {150\over11}\approx13.64
$$
#### (b)
Under $H_{0}$,
$$
T^{2}\sim{p(n-1)\over n-p} F_{p,n-p}
$$
in our case, $p=2, n=4$, therefore
$$
T^{2} \sim 3F_{2,2}
$$
#### (c)
According to $F$ distribution,
$$
F_{2,2}(0.05) = 19
$$
Therefore, the reject region
$$
T^{2}>T^{2}(\alpha) = 3F_{2,2}(0.05) = 57
$$
It's evident that
$$
T^{2}= 13.64 < 57
$$
So we cannot reject $H_{0}$
### Prob. 3
According to Prob.2, the confidence region
$$
\begin{align*}
&T^{2}\le 57\\
\implies& 4\begin{bmatrix}6-\mu_{1} & 10-\mu_{2}\end{bmatrix}\left({1\over 22}\begin{bmatrix}
9 & 15\\
15 & 36
\end{bmatrix}\right)\begin{bmatrix}6-\mu_{1}\le57\\
10-\mu_{2}\end{bmatrix}\\
\implies& {2\over 11}\left[
9(6-\mu_{1})^{2}+30(6-\mu_{1})(10-\mu_{2})+36(10-\mu_{2}) 
\right]\le57\\
\implies& 9(6-\mu_{1})^{2}+30(6-\mu_{1})(10-\mu_{2})+36(10-\mu_{2}) \le 313.5
\end{align*}
$$
which is an ellipse on the $\mu_{1}-\mu_{2}$ plane, where $\mu_{1},\mu_{2}$ are the components of the population mean.
### Prob. 4
The quantities of usage
$$
\begin{gathered}
\boldsymbol{a}_{1}'\overline{\boldsymbol{X}} = \begin{bmatrix}0.5 & 0.5\end{bmatrix}\begin{bmatrix}6 \\ 10\end{bmatrix} = 8
\\
{\rm Var}(\boldsymbol{a}_{1}'\overline{\boldsymbol{X}}) = {\boldsymbol{a}_{1}' S \boldsymbol{a}_{1}\over n} = {5\over 24}=0.2083
\\
{\rm SE}(\boldsymbol{a}_{1}' \overline{\boldsymbol{X}}) = \sqrt{{5\over 24}} = 0.4564
\\
\boldsymbol{a}_{2}'\overline{\boldsymbol{X}} = 10
\\
{\rm Var}(\boldsymbol{a}_{2}'\overline{\boldsymbol{X}})= {\boldsymbol{a}_{2}' S \boldsymbol{a}_{2}\over n}= 0.5
\\
{\rm SE}(\boldsymbol{a}_{2}' \overline{\boldsymbol{X}}) = {1\over \sqrt{2}} = 0.7071
\end{gathered}
$$
The multipliers for different confidence regions are shown below, using parameters $n=4, p=2,\alpha=0.05, m=2$:
$T^2$:
$$
c = \sqrt{{p(n-1)\over n-p}F_{p,n-p}(0.05)} = \sqrt{57} = 7.550
$$
Bonferroni:
$$
t_{n-1}({0.05\over 2\times 2}) = t_{3}(0.0125) = 4.177
$$
Single:
$$
t_{n-1}({0.05\over 2}) = t_{3}(0.025) = 3.182
$$
By the multipliers above, the confidence region for $\boldsymbol{a}_{1}'\boldsymbol{\mu}$ and $\boldsymbol{a}_{2}'\boldsymbol{\mu}$ can be calculated as below:

|            | $\boldsymbol{a}_{1}'\boldsymbol{\mu}$ | $\boldsymbol{a}_{1}'\boldsymbol{\mu}$ |
| ---------- | ------------------------------------- | ------------------------------------- |
| $T^2$      | $[4.554,11.446]$                      | $[4.661,15.339]$                      |
| Bonferroni | $[6.094,9.906]$                       | $[7.047,12.953]$                      |
| Single     | $[6.547,9.453]$                       | $[7.750,12.250]$                      |
### Prob. 5
The test statistics for $H_{0}: C \boldsymbol{\mu}=\boldsymbol{r}$ could be constructed by using a random variable as below:
$$
C \boldsymbol{X}\sim \mathcal{N}_{k}(C \boldsymbol{\mu}, C'\Sigma C)
$$
where we used the condition that $rank(C) = k$
Now we can perform $T^{2}$ test for $C \boldsymbol{\overline{X}}$:
$$
T^{2} = n(\boldsymbol{\mu}-\overline{\boldsymbol{X}})'C' (C'\Sigma C)^{-1} C(\boldsymbol{\mu} - \overline{\boldsymbol{X}})
$$
The distribution of $T^{2}$:
$$
T^{2}\sim {p(n-1)\over n-p}F_{p,n-p}
$$
The rank of $C \boldsymbol{X}$ is $k$, therefore
$$
T^{2}\sim {k(n-1)\over n-k}F_{k,n-k}
$$
### Prob. 6
The hypothesis could be expressed as
$$
\begin{bmatrix}
1 & 0 & -6 \\ 0 & 1 & -4
\end{bmatrix}\begin{bmatrix}
\mu_{1} \\ \mu_{2} \\ \mu_{3}
\end{bmatrix} =
C \begin{bmatrix}
\mu_{1} \\ \mu_{2} \\ \mu_{3}
\end{bmatrix}
= \begin{bmatrix}0 \\ 0\end{bmatrix} = \boldsymbol{\mu}_0
$$
where
$$
\begin{gathered}
C = \begin{bmatrix}
1 & 0 & -6 \\ 0 & 1 & -4
\end{bmatrix}
\\
\boldsymbol{\mu}_{0} = \begin{bmatrix}0 \\ 0\end{bmatrix}
\end{gathered}
$$
Now we can define $H_{0}$
$$
H_{0}: C \boldsymbol{\mu} = \boldsymbol{\mu}_{0}
$$
The test statistics
$$
T^{2} = n (C \overline{\boldsymbol{X}} - \boldsymbol{\mu}_{0})' (C' \Sigma C)^{-1} (C \overline{\boldsymbol{X}} - \boldsymbol{\mu}_{0})
$$
Herein, $p=2, n=6$, therefore
$$
\begin{gathered}
T^{2}\sim {p(n-1)\over n-p}F_{p,n-p}
\\
T^{2}\sim {5\over 2}F_{2,4}
\end{gathered}
$$
Using the data provided, we get that 
$$
T^{2} = 47.143 > {5\over 2}F_{2,4}(0.05) = 17.36
$$
So $H_{0}$ is rejected under significance level of $0.05$.