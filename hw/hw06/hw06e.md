# hw06e

## custom.02
Suppose you have the pulse $$p(t)=\tfrac{1}{\sqrt{T}}\text{sinc}{\left(\tfrac{t}{T}\right)}$$.
You transmit a $$0$$ by sending $$-p(t)$$ and you transmit a $$1$$ by sending $$p(t)$$.  Suppose you have a 1-shot system, i.e. you only said 1 bit and then you close down the transmitter.
So $$x(t)=c_kp(t)$$ where $$c=\pm1$$. Also assume that $$\int{p^2(t)dt}=1$$

**(a)** Show that $$\int{x_z(t)p(t)dt}=c_k$$.

**(b)** What is the bandwidth of this system?  You can leave your answers in terms of $$T$$.

**(c)** What is the bit rate of this system?

**(d)** Suppose you receive $$y_z(t)=x_z(t)+n_I(t)+jn_Q(t)$$.  Your receiver has the following set of operations. First you filter then you take the real part.  So your decision variable is $$Z=\Re{\left(\int{y_z(t)p(t)dt}\right)}$$.

**(i)** Find the energy of the signal (ignoring the noise).

**(ii)** Find the energy of the noise and give an expression for the SNR.

**(iii)** Your rule is if $$Z>0$$, a $$1$$ was sent, if $$Z<0$$, a $$0$$ was sent. What is the probability of error?
