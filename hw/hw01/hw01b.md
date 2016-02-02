# **hw01b**

## 2.3
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

#### 2.3.1.
$$
    \begin{align*}
    y_1(t)&=x_1(t)\cos(2\pi{f_c}t)\\
    &=\left(m(t)\cos{(2\pi{f_c}t)}\right)\cos{(2\pi{f_c}t)}\\
    &=m(t)\cos^2{(2\pi{f_c}t)},&&\left<\cos^2{(\theta)}=\frac{1}{2}\left[1+\cos{(2\theta)}\right]\right>\\
    &=m(t)\left(\frac{1}{2}\left[1+\cos{(2\pi(2){f_c}t)}\right]\right)\\
    &=\frac{1}{2}m(t)+\frac{1}{2}m(t)\cos{(2\pi2f_ct)}
    \end{align*}
$$

#### 2.3.2
$$
    \begin{align*}
    y_2(t)&=x_1(t)\sin(2\pi{f_c}t)\\
    &=\left(m(t)\cos{(2\pi{f_c}t)}\right)\sin{(2\pi{f_c}t)}&&\left<\sin{(2\theta)}=2\cos{(\theta)}\sin{(\theta)}\right>\\
    &=m(t)\left(\frac{1}{2}\left[\sin{(2\pi(2){f_c}t)}\right]\right)\\
    &=\frac{1}{2}m(t)\sin{(2\pi2f_ct)}
    \end{align*}
$$

#### 2.3.3
$$
    \begin{align*}
    y_3(t)&=x_2(t)\cos(2\pi{f_c}t)\\
    &=\left(m(t)\sin{(2\pi{f_c}t)}\right)\cos{(2\pi{f_c}t)}&&\left<\sin{(2\theta)}=2\cos{(\theta)}\sin{(\theta)}\right>\\
    &=m(t)\left(\frac{1}{2}\left[\sin{(2\pi(2){f_c}t)}\right]\right)\\
    &=\frac{1}{2}m(t)\sin{(2\pi2f_ct)}
    \end{align*}
$$


#### 2.3.4
$$
    \begin{align*}
    y_4(t)&=x_2(t)\sin(2\pi{f_c}t)\\
    &=\left(m(t)\sin{(2\pi{f_c}t)}\right)\sin{(2\pi{f_c}t)}\\
    &=m(t)\sin^2{(2\pi{f_c}t)},&&\left<\sin^2{(\theta)}=\frac{1}{2}\left[1-\cos{(2\theta)}\right]\right>\\
    &=m(t)\left(\frac{1}{2}\left[1-\cos{(2\pi(2){f_c}t)}\right]\right)\\
    &=\frac{1}{2}m(t)-\frac{1}{2}m(t)\cos{(2\pi2f_ct)}
    \end{align*}
$$
