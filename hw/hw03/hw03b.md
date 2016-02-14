# hw03b

##2.
**4.5(modified)**

The picture of a color television set proposed by the National Television System Committee (NTSC) is composed by scanning in a grid pattern across the screen.  The scan is made up of three independent beams (red, green, and blue).  These independent beams can be combined to make any color at a particular position.  In order to make the original color transmission compatible with black and white televisions the three color signals  are transformed into a luminance signal (black and white level), $$x_L(t)$$, and two independent chrominance signals, $$x_I(t)$$ and $$x_Q(t)$$. These chrominance signals $$\left(x_r(t),\:\:x_g(t),\:\:x_b(t)\right) $$ are modulated onto a carrier of $$3.58\:\text{MHz}$$ to produce a bandpass signal for transmission.  A commonly used tool for video engineers to understand these coloring patterns is the vectorscope representation shown in **Figure 4.14**.

Write out a baseband TV scan that is: Cyan, Red, Blue, Magenta, Magenta, Cyan.  For example, if I had a TV scan that was Cyan, Red, Cyan, it would look like:
$$
x_z(t)=0.64\exp{(j1.07\pi)}\sqcap{\left(\frac{t}{T}\right)}+0.64\exp{(j0.21\pi)}\sqcap{\left(\frac{t-T}{T}\right)}+0.64\exp{(j1.07\pi)}\sqcap{\left(\frac{t-2T}{T}\right)}
$$
where $$T$$ is the time duration of the color.

**(a)** Plot the in-phase and quadrature components of your signal.

**(b)** How might you set up a decoder for the color?

![figure.02](hw03/hw03-fig02.png)


####2(a)


####2(b)
