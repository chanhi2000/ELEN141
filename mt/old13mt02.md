# old13mt02

## 1.
Consider the following signal, $$m(t)=5\cos{(2\pi440t)$+3\sin{(2\pi880t)$+2\sin{(2\pi1320t)}+0.1\cos{(2\pi1760t)}$$.

**(a)** Find the power spectral density of $$m(t)$$.

**(b)** Estimate the bandwidth of $$m(t)$$. Justify your answer.

**(c)** Suppose $$f_d=1000\:\text{Hz}$$. $$f_c=10\:\text{MHz}$$ and $$A_c=10$$.

(i) Estimate the bandwidth of the FM modulated signal (Justify your answer.
(ii) Is the carrier frequency large enough? Explain why or why not.

**(d)** Suppose you used DSB modulation rather than FM modulation, what would the bandwidth of the signal be?


## 2. 
Let $$m(t)=2\cos{(2\pi10t)}$$

**(a)** Write down the passband version of the FM modulated signal.

**(b)** Write down the baseband version of the FM modulated signal. 


## 3.
Let $$W(t)$$ be a zero-mean AWGN process, with $$S_W(f)=10^{−6}$$. Let $$N(t)=h(t)*W(t)$$ where $$h(t)=2W\text{sinc}{(2Wt)}\cos{(2\pi2Wt)}$$.

**(a)** Find the power spectral density of $$N(t)$$.

**(b)** Find the covariance function (also known as correlation function) $$R_N(\tau)$$

**(c)** Find an expression for the covariance between $$N(0)$$ and $$N(0.001)$$ Assume $$W=100\:\text{Hz}$$.


## 4.
Suppose you have two iid zero-mean Gaussian random variables, $$X$$ and $$Y$$ and $$E[X^2]=2$$. Let $$Z=X+Y$$.

**(a)** Find the pdf of $$f_Z(z).

**(b)** Find the pdf of $$f_Z(z|x).


## 5.
Suppose $$x_c(t)=\sqrt{2}A_cm(t)\cos{(2\pi{f}_ct)}$$, where $$m(t)=10\cos{(2\pi880t)}$$, $$A_c=5$$.

Now suppose this is corrupted by additive white Gaussian noise that has been bandpass filtered, *i.e.* you receive $$y_c(t)=x_c(t)+\sqrt{2}n_I(t)\cos{(2\pi{f}_ct)}−\sqrt{2}n_Q(t)\sin{(2\pi{f}_ct)}$$ where $$f_c\gg{W}$$, the bandwidth of the music, and $$S_{n_I}{(f)}=S_{n_Q}{(f)}=0.01\sqcap{\tfrac{f}{2\times1000}}$$

**(a)** Estimate the SNR of the demodulated signal. (Assume you know the phase of the the modulating cosine $$\cos{(2\pi{f}_ct)}$$

**(b)** Can you improve the SNR of the signal and if so by how much?

