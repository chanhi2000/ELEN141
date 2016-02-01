# week04b

## EXPECTED VALUE
$$
    \begin{align*}
    E[\mathbf{X}]=\begin{cases}\sum_{i}\mathbf{X}_iP(\mathbf{X}_i)\\\int{x\cdot{f}_\mathbf{X}(x)dx}\end{cases}
    \end{align*}
$$
- $$E\equiv$$ average of the random variable $$\equiv$$ "mean".

#### BERNOUILLI RANDOM VARIABLE
$$
\begin{align*}
P(X=0)&=p\\
P(X=1)&=1-p\\\\
E[\mathbf{X}]&=p(1)+(1-p)(0)\\&=p;
\end{align*}
$$

#### BINOMIAL RANDOM VARIABLE
$$
\begin{align*}
P(X=k)&=\left(\begin{matrix}n\\k\end{matrix}\right)p^k(1-p)^{n-k}\\
&\left<\left(\begin{matrix}n\\k\end{matrix}\right)=\frac{n!}{(n-k)!k!}\right>\\\\
E[\mathbf{X}]&=\sum_{k=0}^{N}{\left(\begin{matrix}N\\k\end{matrix}\right)(k)\:p^k(1-p)^{N-k}}
\end{align*}
$$

#### UNIFORM DISTRIBUTION
$$
\begin{align*}
f_\mathbf{X}(x)&=\sqcap{\left(x-\frac{1}{2}\right)}\\\\
E[\mathbf{X}]&=\int_{-\infty}^{\infty}(x)\sqcap{\left(x-\frac{1}{2}\right)}\\
&=\int_{0}^{1}{(x)dx}=\frac{1}{2};
\end{align*}
$$

#### GAUSSIAN DISTRIBUTION
$$
\begin{align*}
f_\mathbf{X}(x)&=\frac{1}{\sqrt{2\pi\sigma^2}}\exp{\left[-\frac{(x-m)^2}{2\sigma^2}\right]}\\\\
E[\mathbf{X}]&=\frac{1}{\sqrt{2\pi\sigma^2}}\int_{-\infty}^{\infty}{(x)\exp{\left[-\frac{(x-m)^2}{2\sigma^2}\right]}dx}=\cdots\\
&=m;
\end{align*}
$$

## [LAW OF UNCONSCIOUS STATISTICIAN](https://en.m.wikipedia.org/wiki/Law_of_the_unconscious_statistician)
$$
E[g(\mathbf{X})]=\begin{cases}\underset{\text{continuous}}{\int{g(x)f_{\mathbf{X}}(x)dx}}\\\\\underset{\text{discrete}}{\sum_{i}{g(x_i)f(x_i)}}\end{cases}
$$
e.g.
$$
E[x^3]=\int{(x^3)f_\mathbf{X}(x)dx}
$$
#### VARIANCE
$$
\text{Var}(\mathbf{X})=E[\mathbf{X}^2]-\left(E[\mathbf{X}]\right)^2
$$
- it represents how wide the random variable varies.
- range.

#### STANDARD DEVIATION
$$
    \sigma=\sqrt{\text{Var}(\mathbf{X})}
$$

#### UNIFORM DISTRIBUTION:
$$
\begin{align*}
f_\mathbf{X}(x)&=\sqcap{\left(x-\frac{1}{2}\right)}\\\\
E[\mathbf{X}]&=\cdots=\frac{1}{2}\\
E[\mathbf{X}^2]&=\int{(x^2)\sqcap{\left(x-\frac{1}{2}\right)}dx}\\
&=\int_{0}^{1}{x^2\:dx}=\frac{1}{3};\\
\text{Var}(\mathbf{X})&=\left(\frac{1}{3}\right)-\left(\frac{1}{2}\right)^2=\frac{1}{12};\\
\sigma&=\sqrt{\frac{1}{12}};
\end{align*}
$$

#### GAUSIAN DISTRIBUTION:
$$
\begin{align*}
f_\mathbf{X}(x)&=\frac{1}{\sqrt{2\pi\sigma^2}}\exp{\left[-\frac{(x-m)^2}{2\sigma^2}\right]}\\\\
E[\mathbf{X}]&=\cdots=m\\
E[\mathbf{X}^2]&=\frac{1}{\sqrt{2\pi\sigma^2}}\int_{-\infty}^{\infty}{(x^2)\exp{\left[-\frac{(x-m)^2}{2\sigma^2}\right]}dx}=\cdots\\
&=m^2+\sigma^2;\\
\text{Var}(\mathbf{X})&=\left(m^2+\sigma^2\right)-\left(m\right)^2=\sigma^2;\\
\sigma&=\sqrt{\sigma^2};
\end{align*}
$$

## EXPECTATION
1. 2 random variables are independent if
$$
    P(X\cap{Y})=P(X)P(Y)
$$
2. if there are **2 Gaussian random variables** where 
$$
    \mathbf{X}_1+\mathbf{X}_2=\mathbf{Z},
$$
then 
$$
    f_{\mathbf{Z}}(z)=f_{\mathbf{X_1}}(x_1)*f_{\mathbf{X_2}}(x_2) 
$$
then $$\mathbf{Z}$$ is a Gaussian random variable. (not true on every case).

####EX#1: uniform distribution
$$
\mathbf{X}_1+\mathbf{X}_2=\mathbf{Z}
$$ and 
$$
\begin{align*}
f_{\mathbf{X}}(x)&=\sqcap{(x)}\\
f_{\mathbf{Z}}(z)&=f_{\mathbf{X}_1}(x_1)*f_{\mathbf{X}_2}(x_2)\\
&=\sqcap{(x)}*\sqcap{(x)}\\
&=\wedge{(x)}
\end{align*}
$$

####EX#2: gaussian (not independent)
$$
\begin{matrix}
\mathbf{X}_1\sim{N}(0,1)\\
\mathbf{Z}\sim{N}(0,1)\\\\
\end{matrix}\:\:\:\:\left\{\begin{matrix}\sim:&\text{distributed}\\N:&\text{normal}\\0:&\text{mean}\\1:&\text{variance}\end{matrix}\right\}
$$
- $$\mathbf{X}_1$$ and $$\mathbf{Z}$$ are independent, 
however
$$
\mathbf{X}_2=0.5\mathbf{X}_1+0.5\mathbf{Z}
$$
- $$\mathbf{X}_1$$ and $$\mathbf{X}_2$$ are NOT independent.

## RANDOM VECTOR
$$

$$