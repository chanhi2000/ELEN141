# **hw01a**

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

#### 2.1.1
$$
    \begin{align*}
    \Re{\left[z_1+z_2\right]}&=\Re{\left[x_1+jy_1\right]}+\Re{\left[x_2+jy_2\right]}\\
    &=x_1+x_2\\
    \Re{\left[z_1+z_2\right]}&=\Re{\left[\alpha_1\cos{(\theta_1)+j\left(\alpha_1\sin{(\theta_1)}\right)}\right]}+\Re{\left[\alpha_2\cos{(\theta_2)+j\left(\alpha_2\sin{(\theta_2)}\right)}\right]}\\
    &=\alpha_1\cos{(\theta_1)}+\alpha_2\cos{(\theta_2)}
    \end{align*}
$$
#### 2.1.2
$$
    \begin{align*}
    \left|z_1+z_2\right|&=\left|\left((x_1+x_2)+j(y_1+y_2)\right)\right|=\sqrt{(x_1+x_2)^2+(y_1+y_2)^2}\\
    &=\sqrt{x_1^2+x_2^2+2x_1x_2+2y_1y_2};\\
    \left|z_1+z_2\right|&=\left|\left(\alpha_1\cos{(\theta_1)}+\alpha_2\cos{(\theta_2)}\right)+j\left(\alpha_1\sin{(\theta_1)}+\alpha_2\sin{(\theta_2)}\right)\right|\\
    &=\sqrt{\left(\alpha_1\cos{(\theta_1)}+\alpha_2\cos{(\theta_2)}\right)^2+\left(\alpha_1\sin{(\theta_1)}+\alpha_2\sin{(\theta_2)}\right)^2}\\
    &=\sqrt{\alpha_1^2\cos^2{(\theta_1)}+\alpha_1^2\sin^2{(\theta_1)}+\alpha_2^2\cos^2{(\theta_2)}+\alpha_2^2\sin^2{(\theta_2)}+2\alpha_1\alpha_2\cos{(\theta_1)}\cos{(\theta_2)}+2\alpha_1\alpha_2\sin{(\theta_1)}\sin{(\theta_2)}}\\
    &=\sqrt{\alpha_1^2+\alpha_2^2+2\alpha_1\alpha_2\cos{(\theta_1)}\cos{(\theta_2)}+2\alpha_1\alpha_2\sin{(\theta_1)}\sin{(\theta_2)}}\\
    &\left<\cos{(a)}\cos{(b)}=\frac{1}{2}\left(\cos{(a-b)}+\cos{(a+b)}\right)\right>\\
    &\left<\sin{(a)}\sin{(b)}=\frac{1}{2}\left(\cos{(a-b)}-\cos{(a+b)}\right)\right>
    &=\sqrt{\alpha_1^2+\alpha_2^2+2\alpha_1\alpha_2\left(\frac{1}{2}\left[\cos{(\theta_1-\theta_2)}+\cos{(\theta_1+\theta_2)}\right]\right)+2\alpha_1\alpha_2\left(\frac{1}{2}\left[\cos{(\theta_1-\theta_2)}-\cos{(\theta_1+\theta_2)}\right]\right)},\\
    &=\sqrt{\alpha_1^2+\alpha_2^2+2\alpha_1\alpha_2\cos{(\theta_1-\theta_2)}}
    \end{align*}
$$

#### 2.1.3
$$
    \begin{align*}
    \Im{\left[z_1z_2\right]}&=\Im{\left[(x_1+jy_1)(x_2+jy_2)\right]}=\Im{\left[x_1x_2-y_1y_2+j\left(x_1y_2+x_2y_1\right)\right]}\\
    &=x_1y_2+x_2y_1;\\
    \Im{\left[z_1z_2\right]}&=\Im{\left[\alpha_1\alpha_2e^{j\left(\theta_1+\theta_2\right)}\right]}=\Im{\left[\alpha_1\alpha_2\cos{(\theta_1+\theta_2)}+j\left(\alpha_1\alpha_2\sin{(\theta_1+\theta_2)}\right)\right]}\\
    &=\alpha_1\alpha_2\sin{(\theta_1+\theta_2)};
    \end{align*}
$$

#### 2.1.4
$$
    \arg{\left[z_1z_2\right]}=\arg{\left[\alpha_1\alpha_2e^{j\left(\theta_1+\theta_2\right)}\right]}=\theta_1+\theta_2
$$

#### 2.1.5
$$
    \begin{align*}
    \left|z_1z_2\right|&=\left|(x_1+jy_1)(x_2+jy_2)\right|=\left|\left(x_1x_2-y_1y_2\right)+j\left(x_1y_2+x_2y_1\right)\right|\\
    &=\sqrt{\left(x_1x_2-y_1y_2\right)^2+\left(x_1y_2+x_2y_1\right)^2}\\
    &=\sqrt{x_1^2x_2^2+y_1^2y_2^2-2x_1x_2y_1y_2+x_1^2y_2^2+x_1^2y_2^2+2x_1x_2y_1y_2}\\
    &=\sqrt{x_1^2x_2^2+y_1^2y_2^2+x_1^2y_2^2+x_1^2y_2^2}=\sqrt{(x_1^2+y_1^2)(x_2^2+y_2^2)}\\
    \left|z_1z_2\right|&=\left|\alpha_1\alpha_2e^{j(\theta_1+\theta_2)}\right|=\alpha_1\alpha_2;
    \end{align*}
$$