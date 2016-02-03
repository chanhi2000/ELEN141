# hw04a

##1.
**5.3(modified)**

A message signal is to be transmitted using analog modulation. The message signal Fourier transform has the form
$$
M(f)=\begin{cases}A\left|\sin{\left(\frac{\pi{f}}{W}\right)}\right|&|f|\leq{W}\\0&\text{elsewhere}\end{cases}
$$

**(a)** Compute the value of $$A$$ such that $$E_m$$ is equal to $$1\:\text{J}$$ in a $$1\:\Omega$$ system.

**(b)** Compute the min $$m(t)$$.

**(c)** Compute the max $$|m(t)|$$.

**(d)** Compute the max $$|\frac{d}{dt}m(t)|$$.

> **NOTE**:

> Don’t do part (d). In this problem, it might be easier to find the inverse Fourier transform directly You may want to use the fact that
$$
\int_{0}^{W}{\sin{(2\pi{f}t_0)}e^{-j2\pi{f}t}df}=-\int_{0}^{W}{\sin{(2\pi{f}t_0)}e^{j2\pi{f}t}df};
$$
It’s easiest to use Matlab to find maximum and minimum values in some cases. In addition: Find an expression for $$m(t)$$ and show how you would modulate it using Double sideband modulation and single sideband modulation.


####1(a)


####1(b)


####1(c)


####1(d)