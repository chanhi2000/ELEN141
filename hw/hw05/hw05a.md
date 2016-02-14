# hw05a

## 3.24(modified)
A commonly used expected value in communication system analysis is the characteristic function given as
$$\phi_{\mathbf{X}}(t)=E\left[\exp{(j\mathbf{X}t)}\right]=\int_{-\infty}^{\infty}{ \exp{(jxt)}p_\mathbf{X}(x)dx}$$
**(a)** Show that
$$
E\left[\mathbf{X}\right]=\left.−j\frac{d\:\phi_\mathbf{X}(t)}{dt}\right|_{t=0}
$$

**(b)** Show that
$$
E\left[\mathbf{X}^n\right]=\left.(−j)^n\frac{d^n\:\phi_\mathbf{X}(t)}{dt^n}\right|_{t=0}
$$
The results in parts (a) and (b) are known as the moment generating property of the characteristic function.

**(c)** Show that if $$\mathbf{X}$$ is a Gaussian random variable with mean, $$m_\mathbf{X}$$ , and variance, $$\sigma_\mathbf{X}^2$$, that $$\phi_\mathbf{X}(t)=\exp{(jt\:m_\mathbf{X}-\frac{1}{2}t^2\sigma_\mathbf{X}^2)}$$.

*Hint*: For any $$b$$
$$
\int_{-\infty}^{\infty}{\frac{1}{\sqrt{2\pi\sigma_\mathbf{X}^2}}\exp{\left(-\frac{(x-b)^2}{2\sigma_\mathbf{X}^2}\right)}dx}=1
$$

**(d)** Show that if $$\mathbf{X}_1$$ and $$\mathbf{X}_2$$ are independent random variables then the characteristic function of $$\mathbf{Y}=\mathbf{X}_1+\mathbf{X}_2$$ is $$\phi_{\mathbf{Y}}(t)=\phi_{\mathbf{X}_1}(t)\phi_{\mathbf{X}_2}(t)$$.

**(e)** Since the characteristic function is unique, deduce from the results in part (d) that the sum of two Gaussian random variable is another Gaussian random variable. Identify $$m_\mathbf{Y}$$ and $$\sigma_\mathbf{Y}$$.


