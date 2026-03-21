### Lec 2
Gain the Pattern by Sample

MLE for Multivariate

#### Descriptive Statistics
For the $k$ th feature (column): separately perform average and variance 
$$
Cov(X,Y) = E[(X-E(X))(Y-E(Y))]
$$
$\frac{1}{n-1}$ coeff: no bias, DOF used by the sample mean 

Sample correlation (for 2 different features)
$$
r_{ik}= \frac{s_{ik}}{\sqrt{s_{ii}}\sqrt{s_{kk}}}
$$
describes l**inear relation only** for 2 features.
Sample variances and covariances $S_{ij}$
**Matrix form**
$p$ features, $n$ samples
Covariance:
$$
S = \frac{1}{n-1}\sum_{i=1}^{n}(X_{i}-\overline{X})(X_{i}-\overline{X})^{T}\in \mathbb{R}^{p\times p}
$$
Key trick
$$
\begin{align*}
(X_{i}-\overline{X})=& [(X-\mu)+(\mu-\overline{X})]^{2}\\
\overline{X} &{\rm \ is\ a\ random\ variable\ independent\ of\ }i\\
E[(\overline{X}-\mu)] =& \frac{1}{n}{\rm Var}(X)
\end{align*}
$$
Expectation is linear:
$$
E(AX) = AE(X)
$$
Variance:
$$
\begin{align*}
Var(X) =& E[(X-\boldsymbol{\mu})(X-\boldsymbol{\mu})']\\
Var(AX) =& A E[(X-\boldsymbol{\mu})(X-\boldsymbol{\mu})'] A'
\end{align*}
$$
#### Multivariate Normal Distribution (MVN)

$$
\begin{align*}
X\sim& N_{p}(\mu,\Sigma)\\
f(x)=&\frac{1}{(2\pi)^{\frac{p}{2}}|\Sigma|^{\frac{1}{2}}}\exp[-\frac{(x-\mu)'\Sigma^{-1}(x-\mu)}{2}]
\end{align*}
$$
and we know that
$$
Y= \Sigma^{-\frac{1}{2}}(X-\mu)\sim N_{p}(0, I)
$$
p-dimension: Contours of constant density for $X\sim N_{p}(\mu,\Sigma)$:
$$
(x-\mu)'\Sigma^{-1}(x-\mu)=c^{2}
$$
It has axes $\pm c\sqrt{\lambda_{i}}e_{i}$.
Note: the Mahalanobis Distance uses $\Sigma^{-1}$ but $\Sigma$.
**Equivalent definition**: (???????)
A random vecotr $X$ is distributed as $N_{p}(\mu,\Sigma)$ $\iff$ $a'X$ is distributed as $N(a'\mu,a'\Sigma a), \forall a\in \mathbb{R}^{p}$
**Linear Combination:** 
If $X\sim N(\mu, \Sigma)$, $A'\Sigma A$ is non-singular, then 
$$
AX+d\sim N_{p}(A\mu+d, A'\Sigma A)
$$
#### MLE
Jacobian definition is transpose of mathematical analysis.
$$
\begin{align*}
\frac{\partial}{\partial x}Ax = A'\\
\frac{\partial}{\partial x}x'A = A\\
\frac{\partial}{\partial x}x'x = 2x\\
\frac{\partial}{\partial x}x'Ax = Ax + A'x\\
\frac{\partial z}{\partial x} = \frac{\partial z}{\partial y}\frac{\partial y}{\partial x}\\
\frac{\partial|A|}{\partial A}=|A|A^{-1}\\
\frac{\partial tr(B'A^{-1}B)}{\partial A}=-A^{-1}(BB')A^{-1}
\end{align*}
$$
$$
\begin{align*}
\hat{\mu} = \overline{X}\\
\hat{\sigma} = \frac{\sum_{i}(X_{i}-\hat{\mu})(X_{i}-\hat{\mu})^{T}}{n}\\
\hat{h(\theta)} = h(\hat{\theta})
\end{align*}
$$

MLE: estimator or estimates

Ralevance between MVN is definitely linear.

### Lec 3
!!!!!!! Sampling meaning for sample variance $s^{2}= {1\over n} \sum_{i=1}^{n}(X_{i}-\overline{X})$:  adding variance of new sample to the existing samples. Key deviation trick:
$$
X_{n}-\overline{X}_{n} = X_{n} - {1\over n}((n-1)\overline{X}_{n-1}+X_{n}) 
$$
Key introduced random variables: $Z_{i}$
Wishart distribution: MVN version of $\chi^{2}$ distribution, returns a $p\times p$ matrix
$Z_{1}$ is redefined for suiting the orthogonality of $Z_{i}$ series

$T^{2}$ is robust under scaling (full-rank linear transition)

Confidence region: CRs given by data could cover (partially) the given CR by the probability of confidence probability
!!!!!! Dual relation of hypothesis test & confidence region?

Bonferroni_t is larger 