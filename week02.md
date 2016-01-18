# **week02**

## PARSEVAL'S THEOREM (for FOURIER SERIES)
$$
    P_x=\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{x^2(t)dt}=\sum_{k=-\infty}^{\infty}{\left|X_k\right|^2};
$$
- #### PROOF???
$$
    \begin{align*}
    x(t)&=\sum_{k=-\infty}^{\infty}{X_ke^{\frac{j2\pi{k}t}{T}}}\\
    \frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{\left|x(t)\right|^2dt}&=\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{\left|\left(\sum_{k=-\infty}^{\infty}{X_ke^{\frac{j2\pi{k}t}{T}}}\right)\right|^2dt}\\
    &=\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{\left(\sum_{k=-\infty}^{\infty}{X_ke^{\frac{j2\pi{k}t}{T}}}\right)\left(\sum_{n=-\infty}^{\infty}{X_n^*e^{-\frac{j2\pi{n}t}{T}}}\right)dt}\\
    &=\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{\left(\sum_{k=-\infty}^{\infty}{X_kX_n^*}\sum_{n=-\infty}^{\infty}{e^{-\frac{j2\pi{n}t}{T}}}\right)dt}
    \end{align*}
$$
- ###### EXAMPLE#1: PARSEVAL'S THEOREM
$$
    
$$

## SPECTRAL DENSITY
- #### time-average power correlation
$$
    \begin{align*}
    R_x(\tau)&=\lim_{T\to\infty}{\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{x(t)x^*(t+\tau)dt}}\\
    R_x(0)&=\lim_{T\to\infty}{\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{\left|x(t)\right|^2dt}}
    \end{align*}
$$
- #### time-average energy correlation
$$
    \begin{align*}
    R_x(\tau)&=\int_{-\infty}^{\infty}{x(t)x^*(t+\tau)dt}
    \end{align*}
$$

- #### energy SPECTRAL DENSITY
$$
    \begin{align*}
    \underset{\text{e.s.d. of }x(t)}{G_x(f)}&=\left|X(f)\right|^2\\
    E_x&=\int_{-\infty}^{\infty}{G_x(f)df}\\
    &=\int_{-\infty}^{\infty}{\left|X(f)\right|^2df}\underset{\text{Rayleigh}}{=}\int_{-\infty}^{\infty}{\left|x(t)\right|^2dt}
    \end{align*}
$$

- #### power SPECTRAL DENSITY 
$$
    \begin{align*}
    \underset{\text{p.s.d. of }x(t)}{S_x(f)}&=\mathcal{F}{\left\{R_x(\tau)\right\}}\propto\left|X(f)\right|^2\\

    P_x&=\int_{-\infty}^{\infty}{S_x(f)df}\\
    &=R_x(0)=\lim_{T\to\infty}{\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{\left|x(t)\right|^2dt}}
    \end{align*}
$$
???
- ###### EXAMPLE#1 
given $$x(t)=2\cos{(2\pi{t})}$$, $$f_0=1\:\text{Hz}$$, find the power spectral density of $$x(t)$$
$$
    \begin{align*}
    R_x(\tau)&=\lim_{T\to\infty}{\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{x(t)x^*(t+\tau)dt}}\\
    &=\lim_{T\to\infty}{\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{\left(2\cos{(2\pi{t})}\right)\left(2\cos{(2\pi({t+\tau}))}\right)}}&&\left<f_0=1;\:\:T=\frac{1}{f_0}=1\right>\\
    &=\underset{0}{\underline{\frac{1}{(1)}{\int_{-\frac{(1)}{2}}^{\frac{(1)}{2}}}{\frac{4}{(2)}\cos{\left(4\pi{t}+2\pi\tau\right)}dt}}}+\frac{1}{(1)}\int_{-\frac{(1)}{2}}^{\frac{(1)}{2}}{\frac{4}{(2)}\cos{\left(2\pi\tau\right)}dt}&&\left<\cos{(a)}\cos{(b)}=\frac{1}{2}\left(\cos{(a+b)}-\cos{(a-b)}\right)\right>\\
    &=2\cos{(2\pi\tau)};\\
    S_x(f)&=\mathcal{F}{\left\{R_x(\tau)\right\}}=\mathcal{F}{\left\{\left(2\cos{(2\pi\tau)}\right)\right\}}=\frac{2}{(2)}\left[\delta{(f-f_0)}+\delta{(f+f_0)}\right]&&\left<\mathcal{F}{\left\{\cos{(2\pi{k_0}t)}\right\}}=\frac{1}{2}[\delta{(k-k_0)}+\delta{(k+k_0)}],\right>\\
    &=\left(\delta{(f-1)}+\delta{(f+1)}\right);\\

    \end{align*}
$$

## BANDWIDTH
- #### TERMINOLOGY
    - $$W$$: one-sided bandwidth
    - $$B$$: two-sided bandwidth
- #### $$X_{dB}$$ Bandwidth
    - Find $$W$$ such that $$\forall{f}>W$$,
    $$
        \begin{align*}
        G_x(f)&\leq\frac{\text{max}{\left(G_x(f)\right)}}{10^{\frac{x}{10}}};&&\text{or}\\\\
        S_x(f)&\leq\frac{\text{max}{\left(S_x(f)\right)}}{10^{\frac{x}{10}}};
        \end{align*}
    $$
- #### $$X\%$$ Bandwidth
    - Find $$W$$ such that $$\forall{f}$$,
    $$
        \begin{align*}
        \frac{\int_{-W}^{W}{S_x(f)df}}{\int_{-\infty}^{\infty}{S_x(f)df}}&=\frac{X}{100};&&\text{or}\\\\
        \frac{\int_{-W}^{W}{G_x(f)df}}{\int_{-\infty}^{\infty}{G_x(f)df}}&=\frac{X}{100};
        \end{align*}
    $$
    
## BASEBAND VS. PASSBAND

