# hw05b

## custom.01
Suppose $$\mathbf{Y}_1,\:\cdots,\mathbf{Y}_3$$ are independent, identically distributed Gaussian random variables with mean $$0$$ and variance $$1$$. Let $$\mathbf{X}_1=\mathbf{Y}_1$$ and $$\mathbf{X}_2=0.5\mathbf{X}_1+0.5\mathbf{Y}_2$$ and $$\mathbf{X}_3=0.5\mathbf{X}_2+0.5\mathbf{Y}_3$$

**(a)** Find $$E\left[\mathbf{X}_i\right],\:\:i=1,\cdots,3$$

**(b)** Find the covariance matrix $$\mathbf{R}$$ for $$\mathbf{X}_1,\:\mathbf{X}_2,\:\mathbf{X}_3$$.

**(c)** Find the joint probability density function for $$\mathbf{X}_1,\:\mathbf{X}_2,\:\mathbf{X}_3$$.

**(d)** Find an expression for $$f_{\mathbf{X}_1,\:\mathbf{X}_2|\:\mathbf{X}_3}(x_1,\:x_2\:|x_3)$$

**(e)** Using the mesh function in Matlab, plot $$f(\mathbf{X}_1,\:\mathbf{X}_2|\:\mathbf{X}_3=0)$$.


## custom.02
Suppose you have an AWGN process $$W(t)$$ with power spectral density $$S_W(f)=\sigma^2$$ This noise is filtered by $$h(t)=\text{sinc}{(t)}+0.5\text{sinc}{(0.5(t −T))}$$ i.e. $$N(t)=h(t)*W(t)$$

**(a)** Find the power spectral density of the filtered noise $$S_N(f)$$.

**(b)** Find the correlation function of $$N(t)$$, $$R_N(\tau)=\mathcal{F}^{-1}(S_N(f))$$.

**(c)** Suppose you have two samples of noise $$N(t)$$ and $$N(t+\tfrac{1}{2})$$ what is the covariance between the two?


## 9.18(modified)
Two noise processes, $$N_1(t)$$ and $$N_2(t)$$, are zero mean, stationary, Gaussian processes, and have the following correlation functions:
$$\begin{matrix}R_{N_1}(\tau)=100\text{sinc}\left(\frac{\tau}{4}\right)&&R_{N_2} (\tau)=50\text{sinc}{(25\tau)}\end{matrix}$$

**(a)** Which random process has a greater power? Why

**(b)** Two samples are taken from $$N_2(t)$$, $$N_2(t_1)$$, and $$N_2(t_1+\tau)$$. What is the smallest value of $$\tau$$ such that the two samples are orthogonal random variables?

**(c)** For $$N_1(t)$$, what is the correlation coefficient corresponding to $$\tau=1$$? Give the joint PDF of two samples of $$N_1(t)$$ taken 1 second apart.

**(d)** Find $$P(N_1(t)<-10)$$.

**(e)** Using only linear devices (amplifiers and filters), generate a random process statistically identical to $$N_1(t)$$ from $$N_2(t)$$.
