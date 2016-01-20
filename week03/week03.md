# **week03**

## LAST TIME
- #### different modulation
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
    \begin{align*}(1+am(t))&>0&&\forall{t}\end{align*}
    $$
        - avg. power of baseband AM signal
        $$
        \begin{align*}
        P_m&=\lim_{T\to\infty}\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{m^2(t)dt}\\
        &=\lim_{T\to\infty}\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{(1+am(t))^2(t)dt}
        \end{align*}
        $$
    


- ####demodulation
- ####envelop detector
    - 
    - why listen to AM radio?

## BACKWARD COMPATIBILITY
- delco radio story (**reflection**):
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


## single-side band mmodulation

