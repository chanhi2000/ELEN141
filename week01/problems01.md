# problems01

##**2.1** 
Let two complex numbers be given as 
$$
    \begin{align*}
    z_1&=x_1+jy_1=\alpha_1\exp{\left(j\theta_1\right)};\\
    z_2&=x_2+jy_2=\alpha_2\exp{\left(j\theta_2\right)};
    \end{align*}
$$

Find
1. $$\Re{\left[z_1+z_2\right]}$$
2. $$\left|z_1+z_2\right|$$
3. $$\Im{\left[z_1z_2\right]}$$
4. $$\arg{\left[z_1z_2\right]}$$
5. $$\left|z_1z_2\right|$$


##**2.3**
Consider the two signals
$$
    \begin{align*}
    x_1(t)=m(t)\cos(2\pi{f_c}t)\\ 
    x_2(t)=m(t)\sin(2\pi{f_c}t)
    \end{align*}
$$
where the bandwidth of m(t) is much less than fc. Compute the simplest form for the following four signals 
1. $$y_1(t)=x_1(t)\cos(2\pi{f_c}t)$$
2. $$y_2(t)=x_1(t)\sin(2\pi{f_c}t)$$
3. $$y_3(t)=x_2(t)\cos(2\pi{f_c}t)$$
4. $$y_4(t)=x_2(t)\sin(2\pi{f_c}t)$$


##**2.5**
This problems exercises the signal and system tools. Compute the Fourier transform of 
$$
    x(t)=\begin{cases}A\sin{\left(\frac{\pi{t}}{T_p}\right)}&0\geq{t}\geq{T_p}\\0&\text{elsewhere}\end{cases}
$$
and give the value of A such that $$E_u=1.$$ Compute the 40-dB relative bandwidth,$$B_{40}$$, of each signal. 


##**2.7**
This problem uses signal and system theory to compute the output of a simple memoryless nonlinearity. An amplifier is an often used device in communication systems and is simply modeled as an ideal memoryless system, i.e., 
$$
    y(t)=\alpha_1x(t)
$$
This model is an excellent model until the signal levels get large then nonlinear things start to happen, which can produce unexpected changes in the output signals. These changes often have a significant impact in a communication system design. As an example of this characteristic consider the system in Figure 2.11 with the following signal model 
$$
    x(t)=b_1\cos{(200000\pi{t})}+b_2\cos{(202000\pi{t})}
$$
the ideal bandpass filter has a bandwidth of 10 kHz centered at 100 kHz, and the amplifier has the following memoryless model 
$$
    y(t)=a_x(t)+a_3x^3(t)
$$
Give the system output, z(t), as a function of $$a_1$$, $$a_3$$, $$b_1$$, and $$b_3$$. 

![figure](week01/img/[ELEN141]hw01-figure01.png)
 


