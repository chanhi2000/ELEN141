# **hw01c**

##**2.5**
This problems exercises the signal and system tools. Compute the Fourier transform of

1.
$$
    x(t)=\begin{cases}A&0\geq{t}\geq{T_p}\\0&\text{elsewhere}\end{cases}
$$
2.
$$
    x(t)=\begin{cases}A\sin{\left(\frac{\pi{t}}{T_p}\right)}&0\geq{t}\geq{T_p}\\0&\text{elsewhere}\end{cases}
$$
and give the value of A such that $$E_u=1.$$ Compute the 40-dB relative bandwidth,$$B_{40}$$, of each signal.


#### 2.5.1

Let $$x(t)=A\sqcap{\left(\frac{t-\frac{T_p}{2}}{T_p}\right)}$$
Then,
$$
    \begin{align*}
    X(f)&=\mathcal{F}{\left\{x(t)\right\}}=\mathcal{F}{\left\{A\sqcap{\left(\frac{t-\frac{T_p}{2}}{T_p}\right)}\right\}},&&\left<\mathcal{F}{\left\{\sqcap{(t)}\right\}}=\text{sinc}{(f)}\right>\\
    &=A\frac{1}{\left|\frac{1}{T_p}\right|}\text{sinc}{\left(\frac{f}{\left|\frac{1}{T_p}\right|}\right)}e^{-j\left(2\pi{f}\left(\frac{T_p}{2}\right)\right)}\\
    &=T_pA\:\text{sinc}{(T_pf)}\:e^{-j\left(2\pi{f}\left(\frac{T_p}{2}\right)\right)}\\
    G_x(f)&=\left|X(f)\right|^2=(T_P)^2(A)^2\text{sinc}^2{(T_pf)};
    \end{align*}
$$
When $$E_u=1$$, we want
$$\int{x^2(t)dt}=1$$. It means
$$
    \begin{align*}
    (T_p)^2(A^2)=1;\\
    A=\sqrt{\frac{1}{T_p}};
    \end{align*}
$$
So
$$
    \begin{align*}
    G_x(f)&=(T_P)^2\left(\sqrt{\frac{1}{T_p}}\right)^2\text{sinc}^2{(T_pf)}\\
    &=T_p\text{sinc}^2{(T_pf)};
    \end{align*}
$$

Find $$W$$ such that,
$$
    \begin{align*}
    \left.G(f)\leq{\frac{\text{max}{(G_x(f))}}{10^{\frac{X}{10}}}}\right|_{X=40}=\underline{\frac{(T_p)}{10^{\frac{40}{10}}}},&&\forall{f}\geq{W}
    \end{align*}
$$
Note that
$$
    \begin{align*}
    G(f)&=T_p\text{sinc}^2{(T_pf)}=T_p\frac{\sin^2{((\pi)T_pf)}}{((\pi)T_pf)^2}\leq\underline{\frac{1}{\pi^2T_p{f}^2}}&&
    \end{align*}
$$
Use these relations now.
$$
    \begin{align*}
    \frac{1}{\pi^2T_p{f}^2}&\leq\frac{T_p}{10^4};\\
    \frac{10^4}{\pi^2T_p^2}&\leq{f}^2;\\
    f&\geq\sqrt{\frac{10^4}{\pi^2T_p^2}}=\frac{10^2}{\pi{T_p}};\\\\
    \therefore{W}&=\frac{10^2}{\pi{T_p}};
    \end{align*}
$$

#### 2.5.2

Let $$x(t)=A\sin{\left(\frac{\pi{t}}{T_p}\right)}\sqcap{\left(\frac{t-\frac{T_p}{2}}{T_p}\right)}$$
Then, find $$A$$ such that,
$$
    \begin{align*}
    \int{x^2(t)dt}&=\int_{0}^{T_p}{\left(A\sin{\left(\frac{\pi{t}}{T_p}\right)}\right)^2dt},&&\left<\sin^2{(\theta)}=\frac{1}{2}\left[1-\cos{(2\theta)}\right]\right>\\
    &=A^2\int_{0}^{T_p}{\frac{1}{2}\left[1-\cos{\left(2\left(\frac{\pi{t}}{T_p}\right)\right)}\right]dt}\\
    &=\frac{A^2}{2}\int_{0}^{T_p}{dt}-\underset{0}{\underline{\frac{A^2}{2}\int_{0}^{T_p}{\cos{\left(\frac{2\pi{t}}{T_p}\right)}dt}}}\cdots\\
    &=\frac{A^2T_p}{2}=1;\\\\
    \therefore{A}&=\sqrt{\frac{2}{T_p}};
    \end{align*}
$$
Now,
$$
    \begin{align*}
    x(t)&=\left(\sqrt{\frac{2}{T_p}}\right)\sin{\left(\frac{\pi{t}}{T_p}\right)}\sqcap{\left(\frac{t-\frac{T_p}{2}}{T_p}\right)},&&\left<\sin{(\theta)}=\cos{(\theta-\frac{\pi}{2})}\right>\\
    &=\left(\sqrt{\frac{2}{T_p}}\right)\cos{\left(\frac{\pi{\left(t-\frac{T_p}{2}\right)}}{T_p}\right)}\sqcap{\left(\frac{t-\frac{T_p}{2}}{T_p}\right)}\\
    X(f)&=\mathcal{F}{\left\{x(t)\right\}}=\mathcal{F}{\left\{\left(\sqrt{\frac{2}{T_p}}\right)\cos{\left(\frac{\pi{t}}{T_p}\right)}\sqcap{\left(\frac{t}{T_p}\right)}\right\}},&&\left<\mathcal{F}{\left\{\cos{\left(\frac{\pi{t}}{T_p}\right)}\sqcap{\left(\frac{t}{T_p}\right)}\right\}}=\frac{T_p}{2}\left[\text{sinc}{\left({T_p}\left(f-\frac{1}{2T_p}\right)\right)}+\text{sinc}{\left({T_p}\left(f+\frac{1}{2T_p}\right)\right)}\right]\right>\\
    &=\sqrt{\frac{2}{T_p}}\left(\frac{T_p}{2}\right)\left[\text{sinc}{\left({T_p}\left(f-\frac{1}{2T_p}\right)\right)}+\text{sinc}{\left({T_p}\left(f+\frac{1}{2T_p}\right)\right)}\right]e^{-j2\pi\left(\frac{T_p}{2}\right)f}\\
    &=\sqrt{\frac{T_p}{2}}\left[\underline{\text{sinc}{\left({T_p}\left(f-\frac{1}{2T_p}\right)\right)}}+\underline{\text{sinc}{\left({T_p}\left(f+\frac{1}{2T_p}\right)\right)}}\right]e^{-j2\pi\left(\frac{T_p}{2}\right)f}\\
    &=\cdots
    \end{align*}

$$
Simplify those terms
$$
    \begin{align*}
    \text{sinc}{\left({T_p}\left(f+\frac{1}{2T_p}\right)\right)}&=\frac{\sin{\left((\pi)\left({T_p}\left(f+\frac{1}{2T_p}\right)\right)\right)}}{(\pi)\left({T_p}\left(f+\frac{1}{2T_p}\right)\right)}\frac{(2)}{(2)}\\
    &=2\frac{\sin{\left(\pi{T_p}f+\frac{\pi}{2}\right)}}{\pi\left(2T_p{f}+1\right)}=2\frac{\cos{\left(\pi{T_p}f\right)}}{\pi\left(2T_p{f}+1\right)}\\
    \text{sinc}{\left({T_p}\left(f-\frac{1}{2T_p}\right)\right)}&=\frac{\sin{\left((\pi)\left({T_p}\left(f-\frac{1}{2T_p}\right)\right)\right)}}{(\pi)\left({T_p}\left(f-\frac{1}{2T_p}\right)\right)}\frac{(2)}{(2)}\\
    &=2\frac{\sin{\left(\pi{T_p}f-\frac{\pi}{2}\right)}}{\pi\left(2T_p{f}-1\right)}=-2\frac{\cos{\left(\pi{T_p}f\right)}}{\pi\left(2T_p{f}-1\right)}
\end{align*}
$$
Back to $$X(f)$$
$$
    \begin{align*}
    X(f)&=\cdots=\sqrt{\frac{T_p}{2}}\left[\left(2\frac{\cos{\left(\pi{T_p}f\right)}}{\pi\left(2T_p{f}+1\right)}\right)+\left(-2\frac{\cos{\left(\pi{T_p}f\right)}}{\pi\left(2T_p{f}-1\right)}\right)\right]e^{-j2\pi\left(\frac{T_p}{2}\right)f}\\
    &=\left(\frac{2}{\pi}\right)\sqrt{\frac{T_p}{2}}\cos{(\pi{T_p}f)}\left[\frac{1}{2T_p{f}+1}-\frac{1}{2T_p{f}-1}\right]e^{-j2\pi\left(\frac{T_p}{2}\right)f}\\
    &=\left(\frac{2}{\pi}\right)\sqrt{\frac{T_p}{2}}\cos{(\pi{T_p}f)}\left[\frac{(2T_p{f}-1)-(2T_p{f}+1)}{(2T_p{f}+1)(2T_p{f}-1)}\right]e^{-j2\pi\left(\frac{T_p}{2}\right)f}\\
    &=\left(\frac{2}{\pi}\right)\sqrt{\frac{T_p}{2}}\cos{(\pi{T_p}f)}\left[\frac{(-2)}{(2T_p{f})^2-1}\right]e^{-j2\pi\left(\frac{T_p}{2}\right)f}
    &=\left(\frac{2}{\pi}\right)\sqrt{\frac{T_p}{2}}\cos{(\pi{T_p}f)}\left[\frac{(2)}{(1-2T_p{f})^2}\right]e^{-j2\pi\left(\frac{T_p}{2}\right)f}
    \end{align*}
$$
