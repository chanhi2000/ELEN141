#**week01**
## REVIEW OF LINEAR SYSTEMS (Ch: 1-2)
1. Convolution
2. Fourier Transforms 
3. Power Spectral Density 
4. Random processes 

## ANALOG VS. DIGITAL
#### ANALOG
- AM radio
- FM radio
- landline phone
- analog TV
- vinyl records
- voice

#### DIGITAL
- telegraph (morse code)
- Wi-Fi / Ethernet 
- TV/cable (digital now, analog back then)
- router/modem
- handwriting
- carrier-pigeon
- smoke-signal
- sign language

#### DIFF(ANALOG, DIGITAL)
- analog is based on **voice** and **music**
- digital is based on **discrete samples** and **finite alphabet/code**

## EXAMPLE: ANALOG VS. DIGITAL
#### VOICE: PRESSURE / ACOUSTIC WAVES
- **microphone (analog)**: use diaphragm.
- **speaker (digital)**: reproduce mechanical sound

#### DIGITAL: BREAKING INTO DISCRETE SAMPLES
- telegraph: **finite alphabets**
- Wi-Fi / Ethernet: **bits**
- carrier-pigeon: pigeon(message with alphabets)


## HISTORY
- #### 1800-1837
    - Fourier analysis
    - Early telegraph systems developed by *Gauss*, *Weber*, *Wheatstone*
- #### 1838-3866
    - Morse telegraph (digital)
- #### 1845
    - KCL and KVL
- #### 1876-1899
    - Acoustic transducer by *Alexander Graham Bell*
    - first telephone exchange in New Haven 8 lines (1878);
- #### 1887-1907
    - Wireless telegraphy, *Marconi* – commercial ship-to-shore and transatlantic systems.
- #### 1904-1920
    - *Lee de Forest* invents the Audio that can amplify AC current. 
    - Experimental AM broadcasting / transcontinental telephone line (1915).
    - *Edwin Armstrong* introduces the superheterodyne radio receiver. 
    - First commercial broadcast.
- #### 1923-1938 
    - Early television by *Philo T. Farnsworth* of San Francisco
- #### 1927 
    - FCC established
- #### 1936
    - *Edwin A. Armstrong* makes the case for FM
- #### 1937 
    - Pulse code modulation, first digital system
- #### 1938-1945
    - Radar and microwave; FM used for military communications
- #### 1944-1950 
    - start of digital communications, information theory – random processes by *Shannon* (1948) 
    - Error-control codes by *Golay* (1950)
- #### 1948-1951 
    - Transistors by Shockley 
- #### 1950
    - Time division multiplexing applied to telephones
- #### 1953 
    - Color TV standards developed in the US
- #### 1955 
    - Satellite communications (sputnik)
- #### 1956 
    - First transoceanic telephone cable
- #### 1962 
    - Telstar – first satellite communications
- #### 1962-1966
    - High speed (?) digital becomes feasible, error-control coding advances
- #### 1965 
    - Mariner IV transmits pictures from Mars
- #### 1966-1975
    - Cable TV, satellite links, ARPAnet (now the internet)

## LINEAR SYSTEM
* #### deterministic signal
* #### random signal (noise)
 
## DETERMINISTIC SIGNAL
* $$\sqcap(t)=\begin{cases}1,&\text{if }t\in\left[-\frac{1}{2},\frac{1}{2}\right]\\0,&\text{otherwise}\end{cases}$$
* $$\text{sinc}(t)=\left(\frac{\sin{(\pi t)}}{\pi t}\right)$$
* $$\cos{\left(2\pi f_ct\right)}$$
* $$\sin{\left(2\pi f_ct\right)}$$
* $$\delta(t)=\begin{cases}\infty,&\text{if }t=0,\\0,&\text{otherwise}\end{cases}$$

#### **EXAMPLE**: DETERMINISTIC SIGNAL 

$$
    \delta_T(t)=\frac{1}{T}\Pi\left(\frac{t}{T}\right)
$$
 
$$
    \delta(t)=\lim_{T\to0}{\frac{1}{T}\Pi\left(\frac{t}{T}\right)}
$$

## PERIODIC SINGALS
* $$x(t)$$ is periodic with period $$T$$, if $$x(t+T)=x(t) \:\:\:\forall{t}$$.

#### LINEARITY
* a function or process is linear if 
$$
H\left[(ax(t)+by(t)\right]=aH\left[x(t)\right]+bH\left[y(t)\right]
$$

* For example, convolution is linear.
$$
    \underset{\text{convolution}}{x(t)*h(t)=\int_{\infty}^{\infty}{x(\tau)h(t-\tau)d\tau}=\int_{\infty}^{\infty}{x(t-\tau)h(\tau)d\tau}}
$$

#### DELTA FUNCTION: SIFTING PROPERTY
$$
\begin{align*}
\delta(t)∗h(t)&=h(0)\int_{-\infty}^{\infty}δ(t−T_0)h(t)dt\\
&=h(T)
\end{align*}
$$

## FOURIER TRANSFORM
$$
\mathcal{F}\left\{x(t)\right\}\triangleq\int_{-\infty}^{\infty}x(t)e^{−j2π(f)t}dt=X(f)
$$
*  The Fourier transform pulls out the frequency components of a signal. 
*  Very important for communications as we need to know the frequency components of a signal. 
*  **e.g.** AM 810 kHz, FM 91.7 MHz etc.
------------------
#### INNER PRODUCT 
> projecting one function onto another function

* **discrete inner product**: e.g. dot product
$$
\underset{\text{dot product}}{\left<\vec{x},\vec{y}\right>=\sum_{i=1}^{N}{x_iy_i}}
$$
* **continuous innner product**:
$$
\underset{\text{fourier transform}}{\left<x(t),y(t)\right>=\int_{-\infty}^{\infty}{x(t)\underline{y(t)}dt}}\:\:\:\:\left<y(t)=e^{-j12\pi(f)t}\right>
$$
----------------------
#### 01. RECT FUNCTION 
$$
    \mathcal{F}\left\{\sqcap{(t)}\right\}=\text{sinc}(t)
$$
 
#### 02. SUPERPOSITION LINEARITY
$$
    \mathcal{F}\left\{ax(t)+by(t)\right\}=aX(f)+bY(f)
$$

* ###### EXAMPLE:
    
$$
    \begin{align*}
    x(t)&=\sqcap{\left(\frac{t}{4}\right)}+\sqcap{\left(\frac{t}{2}\right)}\\
    X(f)&=\mathcal{F}\left\{x(t)\right\}\\
    &=4\text{sinc}{\left(4f\right)}+4\text{sinc}{\left(2f\right)}
    \end{align*}
$$

#### 03. TIME DELAY
$$
    \mathcal{F}\left\{x(t-a)\right\}=X(f)e^{-j2\pi{f}a}
$$

#### 04. SCALE CHANGE
$$
    \mathcal{F}\left\{ax(t)\right\}=\frac{1}{\left|a\right|}X\left(\frac{f}{a}\right)
$$
* ###### EXAMPLE:
$$
    \mathcal{F}\left\{\sqcap{\left(\frac{t}{10}\right)}\right\}=(10)\text{sinc}{\left(f\cdot10\right)}
$$

#### 05. DUALITY
* if i know the FT in one direction, then I know the other.
$$
    \mathcal{F}\left\{X(t)\right\}=x(-f)
$$

* ###### EXAMPLE:
$$
    \begin{align*}
    \mathcal{F}\left\{\sqcap{(t)}\right\}&=\text{sinc}(f)\\
    \mathcal{F}\left\{\text{sinc}(f)\right\}&=\sqcap{\left(-f\right)}=\sqcap{\left(f\right)}
    \end{align*}
$$
 
#### 06. FREQUENCY TRANSLATION   
$$
    \mathcal{F}\left\{x(t)e^{j2\pi{f}_0t}\right\}=X(f-f_0)
$$

#### 07. MODULATION THEOREM 
$$
    \mathcal{F}\left\{x(t)\cos{\left(j2\pi{f}_0t\right)}\right\}=\frac{1}{2}\left[X(f-f_0)+X(f+f_0)\right]
$$

#### 08. DIFFERENTIATION
$$
    \mathcal{F}\left\{x'(t)\right\}=j2\pi{f}X(f)
$$
- derivative **amplifies** frequency

#### 09. INTEGRATION
$$
    \mathcal{F}\left\{\int_{-\infty}^{t}x(\tau)d\tau\right\}=\frac{X(f)}{j2\pi{f}}+\frac{1}{2}X(f)\delta(f)
$$
- integral **smooth down** frequency

#### 10. CONVOLUTION
$$
    \mathcal{F}\left\{x(t)*h(t)\right\}=X(f)H(f)
$$

* ###### EXAMPLE
$$
    \begin{align*}
    \text{sinc}{(t)}*\text{sinc}{(t)}&=\int_{-\infty}^{\infty}{\text{sinc}{(t-\tau)}\text{sinc}{(t)}d\tau}\\
    &=\cdots\text{ugly}\\
    \mathcal{F}\left\{\text{sinc}{(t)}*\text{sinc}{(t)}\right\}&=\sqcap{(f)}\sqcap{(f)}=\sqcap{(f)}\\
    \mathcal{F}^{-1}\left\{\mathcal{F}\left\{\text{sinc}(t)*\text{sinc}(t)\right\}\right\}&=\mathcal{F}^{-1}\left\{\sqcap{(f)}\right\}\\
    &=\text{sinc}{(t)}
    \end{align*}
$$


#### 11. MULTIPLICATION
$$
    \mathcal{F}\left\{x(t)h(t)\right\}=X(f)*H(f)
$$

#### 12. RAYLEIGH'S THEOREM
$$
    \int_{-\infty}^{\infty}{x(t)y^*(t)dt}\triangleq\int_{-\infty}^{\infty}{X(f)Y^*(f)df}
$$
* ###### PROOF

$$
    \begin{align*}
    \int_{-\infty}^{\infty}{x(t)y^*(t)dt}&=\int_{-\infty}^{\infty}{\int_{-\infty}^{\infty}{X(f)e^{j2\pi(f)t}dt}\int_{-\infty}^{\infty}{Y^*(\lambda)e^{-j2\pi(f)\lambda{t}}d\lambda\:dt}}\\
    &=\int_{-\infty}^{\infty}{\int_{-\infty}^{\infty}{X(f)Y^*(\lambda)}\int_{-\infty}^{\infty}{e^{j2\pi(f-\lambda)t}dt}}\\
    &=\int_{-\infty}^{\infty}{\int_{-\infty}^{\infty}{X(f)Y^*(\lambda)\delta(f-\lambda)df\:d\lambda}}\\
    &=\int_{-\infty}^{\infty}{X(f)Y^*(f)};
    \end{align*}
$$

* ###### EXAMPLE

$$
    \int_{-\infty}^{\infty}{\text{sinc}^2{(t)}dt}=\int_{-\infty}^{\infty}{\sqcap(f)\underset{=\sqcap^*(f)}{\underline{\sqcap(f)}}df}=1
$$

## TIME-AVERAGE AUTO CORRELATION
$$
    R(\tau)=\lim_{T\to\infty}{\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{x(t)x(t+\tau)dt}}
$$
$$
    \begin{align*}
    R(0)&=\lim_{T\to\infty}{\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{x(t)x(t)dt}}=\underset{\text{average power}}{\underline{\lim_{T\to\infty}{\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{\left|x(t)\right|^2dt}}}}\end{align*}
$$

## POWER VS. ENERGY
#### POWER
$$
    \begin{align*}
    P&=V\cdot{I}\\&=I^2\cdot{R}\\&=\frac{V^2}{R}
    \end{align*}
$$
- The power per Ohm is $$I^2$$. when we talk about power, we are talking about a **squared term**. If we assume a **1 Ohm resistor as a reference**, then we can also include $$V^2$$, but we want to be aware of the reference to the resistance. In other words, $$P=V^2=I^2$$.

#### instantaneous POWER
$$
    p(t)=x^2(t)
$$

#### average POWER
$$
    P_x=\lim_{T\to\infty}\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{p(t)dt}
$$
#### ENERGY
$$
    E_x=\int_{-\infty}^{\infty}{p(t)dt}
$$
- Some signals are called "**power**" signals $$(P_x>0)$$
- Some signals are called "**energy**" signals $$(E_x<\infty)$$

###### EXAMPLE#1: P vs. E
$$
    x(t)=\cos{\left(2\pi{f_0}t\right)};
$$
- **instantaneous power**:
$$
    \begin{align*}
    p(t)&=x^2(t)=\cos^{2}{\left(2\pi{f_0}t\right)}&&\left<\cos^2{\theta}=\frac{1}{2}\left(1+\cos{\left(2\theta\right)}\right)\right>\\
    &=\frac{1}{2}\left(1+\cos{\left(2\pi(2){f_0}t\right)}\right)
    
    \end{align*}
$$

- **average power** :
$$
    \begin{align*}P_x&=\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{p(t)dt}=\frac{1}{T}\left[\int_{-\frac{T}{2}}^{\frac{T}{2}}{\frac{1}{2}dt}+\int_{-\frac{T}{2}}^{\frac{T}{2}}{\frac{1}{2}{\cos{\left(2\pi2{f_0}t\right)}}dt}\right]\\
    &=\frac{1}{T}\left[\left.\frac{1}{2}t\right|^{\frac{T}{2}}_{-\frac{T}{2}}+\left.\frac{1}{2}\frac{1}{2\pi2{f_0}}\sin{\left(2\pi2{f_0}t\right)}\right|_{-\frac{T}{2}}^{\frac{T}{2}}\right]\\
    &=\frac{1}{T}\left[\frac{1}{2}\left(\underset{T}{\underline{\frac{T}{2}-\left(-\frac{T}{2}\right)}}\right)+\frac{1}{2\pi4{f_0}t}\left(\underset{0}{\underline{\sin{\left(2\pi2\left(\frac{T}{2}\right)t\right)}}}-\underset{0}{\underline{\sin{\left(2\pi2\left(-\frac{T}{2}\right)t\right)}}}\right)\right]\\
    &=\frac{1}{2};
    \end{align*}
$$

- **energy**
$$
    E_x=\int_{-\infty}^{\infty}{p(t)dt}=\infty
$$
- is it **power signal** or **energy signal**?
$$
    \therefore{x(t)}\text{ is power signal}\:\:\:\:\begin{cases}P_x>0\\E_x=\infty\end{cases}
$$

###### EXAMPLE#2: P vs. E
$$
    x(t)=\text{sinc}{(t)};
$$

- **instantaneous power**:
$$
    \begin{align*}
    p(t)&=x^2(t)=\text{sinc}^{2}{(t)}\\
    &=\frac{1}{2}\left(1+\cos{\left(2\pi(2){f_0}t\right)}\right)
    
    \end{align*}
$$
- **average power** :
$$
    \begin{align*}P_x&=\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{p(t)dt}=\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{\text{sinc}^2{(t)}dt}\\
    &=\cdots=0;
    \end{align*}
$$

- **energy**
$$
    \begin{align*}E_x&=\int_{-\infty}^{\infty}{p(t)dt}=\int_{-\infty}^{\infty}{\text{sinc}^2{(t)}dt}\\
    &=\underset{Rayleigh}{\int_{-\infty}^{\infty}{\sqcap{(f)}\sqcap{(f)}df}}=\int_{-\infty}^{\infty}{\sqcap{(f)}df}\\
    &=\cdots=1
    \end{align*}
$$
- is it **power signal** or **energy signal**?
$$
    \therefore{x(t)}\text{ is energy signal}\:\:\:\:\begin{cases}P_x=0\\E_x<\infty\end{cases}
$$

## dB
- dB is **always** referenced to power (given an amplitude of a signal)
- *Communications people* use decibels all the time. **Why?** it's cool and also it's a way to measure signal strength, etc.

$$
    \begin{align*}
    P_{\text{dB}}&=10\log_{10}{\left(A^2\right)}\\
    &=20\log_{10}{\left(A\right)}
    \end{align*}
    
$$
- ###### EXAMPLE: dB
$$
    \begin{align*}
    V&=10\:\text{V};\\
    P&=\left(V\right)^2=\left(10\right)^2=100\:
    \end{align*}
$$
- ###### EASY dB TABLE
 
| $$A^2$$ | dB |
| ------- | -- |
| 1       | 0  |
| 2       | 3  |
| 3       | -  |
| 4       | 6  |
| 5       | 7  |
| 6       | -  |
| 7       | -  |
| 8       | 9  |
| 9       | -  |
| 10      | 10 |

## FOURIER SERIES
- Given $$x(t)$$ which is periodic over some period T, we can approximate it as,
$$
    \begin{align*}
    x(t)&=\sum_{k=-\infty}^{\infty}{X_ke^{\frac{j2\pi{k}t}{T}}},\\
    X_k&=\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{x(t)e^{-\frac{j2\pi{k}t}{T}}dt}\\
    &=\left.\mathcal{F}{\left\{\sqcap{\left(\frac{t}{T}\right)}x(t)\right\}}\right|_{f=\frac{k}{T}}
    \end{align*}
$$
- ###### EXAMPLE#1: FOURIER SERIES
- given the followings:
$$
    \begin{align*}
    T&=2;\\
    x(t)&=\sum_{n=-\infty}^{\infty}{\wedge{\left(t-2n\right)}};&&\left<\underset{\text{triangle function}}{\wedge{(t)}}=\begin{cases}1+t,&t\in\left[-1,0\right]\\1-t,&t\in\left[0,1\right]\\0,&\text{otherwise}\end{cases}\right>;
    \end{align*}
$$
find the Fourier series of such signal.
$$
    \begin{align*}
    X_n&=\frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}{x(t)e^{-\frac{j2\pi{n}t}{T}}dt}=\frac{1}{(2)}\int_{-\frac{(2)}{2}}^{\frac{(2)}{2}}{x(t)e^{-\frac{j2\pi{n}t}{T}}dt}\\
    &=\frac{1}{2}\int_{-\infty}^{\infty}{x(t)e^{-\frac{j2\pi{n}t}{T}}dt}=\left.\frac{1}{2}\mathcal{F}{\left\{\wedge{(t)}\right\}}\right|_{f=\frac{n}{2}}&&\left<\sqcap{(t)}*\sqcap{(t)}=\wedge{(t)}\right>\\
    &=\left.\frac{1}{2}\mathcal{F}{\left\{\sqcap{(t)}*\sqcap{(t)}\right\}}\right|_{f=\frac{n}{2}}=\left.\frac{1}{2}\text{sinc}^2{\left(f\right)}\right|_{f=\frac{n}{2}}&&\left<\mathcal{F}{\left\{\sqcap{(t)}*\sqcap{(t)}\right\}}=\text{sinc}{(f)}\text{sinc}{(f)}\right>\\
    &=\frac{1}{2}\text{sinc}^2{\left(\frac{n}{2}\right)};\\\\
    x(t)&=\sum_{k=-\infty}^{\infty}{X_ke^{\frac{j2\pi{k}t}{T}}}=\sum_{k=-\infty}^{\infty}{\left(\frac{1}{2}\text{sinc}^2{\left(\frac{k}{2}\right)}\right)e^{\frac{j2\pi{k}t}{T}}}\\
    &=\frac{1}{2}+\frac{1}{2}
    \end{align*}
$$