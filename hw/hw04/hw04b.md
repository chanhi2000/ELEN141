# hw04b

##2.
**6.7(modified)**

The Federal Communications Commission (FCC) makes each station strictly limit their output frequency content. Assume AM stations pro- duce a usable audio bandwidth of $$10\:\text{kHz}$$. AM stations in the same geographical area are normally spaced at least 30 kHz apart. As an example of why limits on the frequency content are necessary the following problem is posed.

Consider two stations broadcasting in the same geographic area with a receiver tuned to one of them as shown in **Figure 6.33**. Station A is broad- casting a $$1\:\text{V}$$ peak sinewave of $$2\:\text{kHz}$$, $$m_A(t)$$ (a test of the emergency broadcast system), at a center frequency of $$f_c\:\text{Hz}$$. Station B is broadcasting a $$1\:\text{V}$$ peak $$3\:\text{kHz}$$ square wave, $$m_B(t)$$, at $$f_c+30\:\text{kHz}$$ with no filtering at the transmitter. Since each transmitted waveform will have a different propagation loss, the received waveform is given by the form
$$
\begin{align*}
r_c(t)&=A_A[(1.5+m_A(t))\sqrt{2}\cos{(2\pi{f_c}t+\phi_A)}]\\
&+A_B[(1.5+m_B(t))\sqrt{2}\cos{(2π(f_c+30000)t+\phi_B)}]
\end{align*}
$$
Assume without loss of generality that the phase shift for the station A is zero, i.e., $$\phi_A=0$$.

(a) Give the complex envelope of the received signal, $$r_z(t)$$.

(b) Find the spectrum (Fourier series coefficients)of the complex envelope, $$r_z(t)$$.

(c) The demodulator has an ideal bandpass filter with a center frequency of $$f_c$$ and a two-sided bandwidth of $$2W=15\:\text{kHz}$$ followed by an envelope detector as shown in **Figure 6.33**. Plot the output demodulated waveform, $$\hat{m}_A(t)$$, over $$5\:\text{ms}$$ of time for several values of $$\phi_b$$ in the range $$[0,\:2\phi]$$ and $$A_B=0.1,\:1,\:10$$.

The distortion you see in this example is called adjacent channel interference and one of the FCC’s functions is to regulate the amount of interference each station produces for people trying to receive another station.

![figure.01](hw04/hw04-fig01.png)
> **NOTE**:

> Assume that $$A_A=1$$ and assume that $$m_B(t)$$ is a square-wave with 50% duty cycle. (DC value for $$m_B(t)=\frac{1}{2}$$)


####2(a)


####2(b)


####2(c)
