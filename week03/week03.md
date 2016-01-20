# **week03**

## LAST TIME
- #### MODULATIONS
    - ###### double-side band modulation (DSB)
    $$
    \begin{align*}
    \underset{\text{baseband}}{x_z(t)}&=Am(t)\\
    x_c(t)&=A\sqrt{2}m(t)\cos{2\pi(f_c)t};
    \end{align*}
    $$
    - ###### AM radio
    $$
    \begin{align*}
    \underset{\text{baseband}}{x_z(t)}&=A\left(m(t)\right)\\
    x_c(t)&=A\sqrt{2}m(t)\cos{2\pi(f_c)t};
    \end{align*}
    $$
    where a is chosen so that 
    $$
    \begin{align*}(1+a\:m(t))&>0&&\forall{t}\end{align*}
    $$
        - avg. power of baseband AM signal
        $$
        \begin{align*}
        P_m&=\lim_{T\to\infty}\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{m^2(t)dt}\\
        &=\lim_{T\to\infty}\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{(1+a\:m(t))^2(t)dt}\\
        &=\lim_{T\to\infty}\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{1+2a\:m(t)+a^2m^2(t)dt}\\
        &=1+0+a^2(P_m)
        \end{align*}
        $$
        so
        $$
        P_{xz}=A^2\left(1+a^2P_m\right)
        $$
        - realworld example (in music)
        $$
        \frac{A^2a^2P_m}{A^2\left(1+a^2P_m\right)}\:\:\text{typically at }\frac{1}{3},\:\:\frac{1}{4},\cdots
        $$
        for a boring radio station, it generates a signal such that,
        $$
        m(t)=\cos{\left(2\pi(2\times10^3)t\right)}
        $$
        if $$(1+a\:m(t))>0$$, let's suppose $$a=0.9$$.
        $$
        \begin{align*}
        \frac{A^2a^2P_m}{A^2\left(1+a^2P_m\right)}&=\frac{(0.9)\left(\frac{1}{2}\right)}{1+\left(\frac{1}{2}\right)(0.9)^2}\\
        &<\frac{1}{3}\cdots\:\:\:\text{wasteful}
        \end{align*}
        $$

- #### DEMODULATION
    - ###### 1. 
        - $$x_c(t)=A\sqrt{2}m(t)\cos{(2\pi{f_c}{t})}$$
        - $$\cos{(2\pi{f_c}{t})}$$
        - $$A\sqrt{2}m(t)\left(\frac{1}{2}\right)\left(1+\cos{(2\pi(2f_c){t})}\right)$$
        - $$\frac{A\sqrt{2}}{2}m(t)$$
    
    - ###### 2.
        - $$x_c(t)=A\sqrt{2}m(t)\cos{(2\pi{f_c}{t})}$$
        - $$\cos{(2\pi{f_c}{t}+\theta)}$$
        - $$A\sqrt{2}m(t)\left(\frac{1}{2}\right)\left(\cos{(\theta)}+\cos{(2\pi{(2f_c)}{t}+(\theta))}\right)$$
        - $$\frac{A\sqrt{2}}{2}m(t)\cos{(\theta)}$$
    - ###### 3.
        - $$x_c(t)=A\sqrt{2}m(t)\cos{(2\pi{f_c}{t})}$$
        - $$\cos{(2\pi{(f_c+\Delta{f})}{t}+\theta)}$$
        - $$A\sqrt{2}m(t)\left(\frac{1}{2}\right)\left(\cos{(2\pi\Delta{f}t+\theta)}+\cos{(2\pi{2(f_c+\Delta{f})}{t}+(\theta))}\right)$$
        - $$\frac{A\sqrt{2}}{2}m(t)\cos{((2\pi\Delta{f}t+\theta))}$$

- #### ENVELOP DETECTOR (1920)
    - **full-wave** rectifier: negative -> positive
    - **half-wave** rectifier: take only positive 
    > **Q**:why do we still listen to AM radio?
    > - difficult to transfer (cost, effort)
    > - for consumers
    > - propagation range

## BACKWARD COMPATIBILITY
- Delco radio story (**reflection**):
    - because of consumers and ads, we cannot remove it still.
    - however analog TV is gone (by deadline)!
    - **AM**: propagation
        - wavelength size: (typically 800 KHz) large!
        $$
        \lambda=\frac{c}{f}=\frac{(3.0\times10^{8})}{(8.0*10^5)}=375\:\text{m}
        $$
        - for yourself: see how far away you can get from the AM signal and see if the signal dissipates.
        - they are told to shut down at night (due to interference)
        - **cusack**: why do the AM radio becomes distorted when you are near the power line?
        - **a**: harmonics from the power line distort the signal
    - so your **phone** / **AM Radio** is backward-compatib le because it can deal with a variety of modulation techniques.

## SINGLE-SIDE BAND MODULATION
$$
    \begin{align*}
    x_z(t)&=Am(t)+JA\hat{m}(t)\\
    x_c(t)&=A\sqrt{2}m(t)\cos{\left(2\pi(f_c)t\right)}-A\sqrt{2}\hat{m}(t)\sin{\left(2\pi(f_c)t\right)};
    \end{align*}
$$
 - #### $$\hat{m}(t)$$
    - EXAMPLE: DSB vs. SSB
    if $$m(t)\in\mathbb{R}$$ , $$M(f)=\mathcal{F}{\left\{m(t)\right\}}=M^*(f)$$   
    - $$\hat{m}(t)=\$$
    $$
    $$
