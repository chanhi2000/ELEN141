# **hw01d**

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
Give the system output, $$z(t)$$, as a function of $$a_1$$, $$a_3$$, $$b_1$$, and $$b_3$$. 

![figure](/week01/img/[ELEN141]hw01-figure01.png)