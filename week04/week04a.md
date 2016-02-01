# week04a

## DIGITAL SIGNAL
$$
    x_C(t)=\sqrt{2}x_I(t)\cos{(2\pi{f_c}t)}-\sqrt{2}x_I(t)\cos{(2\pi{f_c}t)}\\
    \begin{cases}
    x_I(t)&=\sum_{n=-\infty}^{\infty}{c_{n,I}p(t-nT)};\\
    x_Q(t)&=\sum_{n=-\infty}^{\infty}{c_{n,Q}p(t-nT)};
    \end{cases}
$$
- $$p$$: pulse train
- $$c_{N_{I,Q}}=\pm1$$;

#### example#1: DIGITAL SIGNAL
suppose you are given a series of bit values such that the bits are shown as $$00001111010110$$. 
- if you separate these bits by two, it would look as following.
$$00\:00\:11\:11\:01\:01\:10$$. 
- In each set, use first bit for *in-phase* and second bit for *quadrature*.  
- Here's how it would look like. Define bits in this following manner.
$$
    \begin{matrix}
    \text{bit}&C_{1,I}&C_{1,Q}\\\hline
    00:&-1&-1\\00:&-1&-1\\11:&1&1\\01:&-1&1\\01:&-1&1\\10:&1&-1\\
    \end{matrix}
$$
- baseband form for this signal would look 
$$
    \begin{align*}
    x_I(t)&=(-1)p(t)+(-1)p(t-T)+(1)p(t-2T)+(-1)p(t-3T)+(-1)p(t-4T)+(1)p(t-5T)\\
    x_Q(t)&=(-1)p(t)+(-1)p(t-T)+(1)p(t-2T)+(1)p(t-3T)+(1)p(t-4T)+(-1)p(t-5T)
    \end{align*}    
$$


##RANDOMNESS OF INFORMATION
$$
    \begin{align*}
    x_z(t)=\sum_{k=-\infty}^{\infty}{c_kp(t-kT)}&&
    \begin{matrix}\text{model }c_k\text{ as a }\\\text{random variable, i.e.}\\ c_k=\pm1\end{matrix}
    \end{align*}
$$
- noise is random too.

## RANDOM VARIABLES
#### PROBABILITY
###### **axiom:**
1. $$P(A)\geq0$$
2. let $$\Omega$$ the set of all possible events, i.e. $$P(\Omega)=1$$
3. $$P(A\cup{B})=P(A)+P(B)-P(A\cap{B})$$;
4. $$P(A|B)=\frac{P(A\cap{B})}{P(B)}$$;
 
###### EX#1: probability.
Given
- $$P(\text{Tx}\:\text{Black})=0.2$$
- $$P(\text{Tx}\:\text{White})=0.8$$

$$
    \begin{align*}
    P(\text{Rx}\:\text{Black})&=P(\text{Rx}\:\text{Black}\:\cap\:\text{Tx}\:\text{Black})+P(\text{Rx}\:\text{Black}\:\cap\:\text{Tx}\:\text{White})\\
    &\left<P(A|B)=\frac{P(A\cap{B})}{P(B)}\:\:\:\:\cdots\:\:\:\:P(A\cap{B})=P(A|B)P(B)\right>\\
    &=P(\text{Rx}\:\text{Black}|\text{Tx}\:\text{Black})P(\text{Tx}\:\text{Black})+P(\text{Rx}\:\text{Black}|\text{Tx}\:\text{White})P(\text{Tx}\:\text{White})\\
    &=(0.9)(0.2)+(0.1)(0.8)=0.26;
    \end{align*}
$$
## DISCRETE RANDOM VARIABLE
$$
\begin{align*}
P(X_i)=a,&&\sum_{n}{P(X_i)}=1;
\end{align*}
$$

#### BERNOUILLI RANDOM VARIABLE
$$
\begin{align*}
P(X=0)&=p\\
P(X=1)&=1-p
\end{align*}
$$

#### BINOMIAL RANDOM VARIABLE
$$
\begin{align*}
P(X=k)=\left(\begin{matrix}n\\k\end{matrix}\right)p^k(1-p)^{n-k}\\\\
\left<\left(\begin{matrix}n\\k\end{matrix}\right)=\frac{n!}{(n-k)!k!}\right>
\end{align*}
$$
i.e. $$n=6$$, $$k=2$$
$$
\left(\begin{matrix}6\\2\end{matrix}\right)=\frac{6!}{4!2!}=\frac{(6)(5)}{(2)(1)}=15
$$

#### GEOMETRIC RANDOM VARIABLE
$$
    P(X=k)=p(1-p)^{k-1}
$$
- **when will it be used?**: how many experiments needed to win?

## CONTINUOUS RANDOM VARIABLE
- **probability density function**:
$$
    \begin{align*}
    f_\mathbf{X}(x)&&\begin{cases}\mathbf{X}:\:\text{random varaible}\\x:\:\text{value that can take on}\end{cases}
    \end{align*}
$$
    - $$P(\mathbf{X}<x)=\int_{-\infty}^{x}{f_\mathbf{X}(s)ds}$$
    - $$P(\mathbf{X}=a)=0;$$
    - $$P(a<\mathbf{X}<b)=\int_{a}^{b}{f_\mathbf{X}(s)ds}$$
- **cumuative distribution function**:
$$
\begin{align*}    
F_\mathbf{X}(x)&=\int_{-\infty}^{x}{f_\mathbf{X}(s)ds}\\
&=P(\mathbf{X}<x)
\end{align*}
$$
    - $$\frac{d}{xd}F_\mathbf{X}(x)=f_X(x)$$
    - $$\int_{-\infty}^{\infty}{f_X(s)ds}=1;$$

#### UNIFORM DISTRIBUTION
$$
    \underset{\text{probability density function}}{f_\mathbf{X}(x)=\sqcap{(x)}}\\
    \underset{\text{cumulative distribution  function}}{F_\mathbf{X}(x)=\sqcap{\left(x-\frac{1}{2}\right)}}
$$
 - $$P(0<\mathbf{X}<\frac{1}{2})=\frac{1}{2}$$.
 - $$P(\mathbf{X}=0.25)=\int_{0.25}^{0.25}{\sqcap{(x)}}=0$$.

#### GAUSSIAN DISTRIBUTION
$$
    \underset{\text{probability density function}}{f_\mathbf{X}(x)=\frac{1}{\sqrt{2\pi\sigma^2}}\exp{\left[-\frac{(x-m)^2}{2\sigma^2}\right]}}\\
    \underset{\text{cumulative distribution  function}}{F_\mathbf{X}(x)=\int_{x}^{-\infty}{f_{\mathbf{X}}(s)ds}}
$$