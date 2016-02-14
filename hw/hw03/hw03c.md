# hw03c

##3.
**4.14**

A commercial airliner is flying 15,000 feet above the ground and pointing its radar down to aid traffic control. A second plane is just leaving the runway as shown in **Figure 4.22**. The transmitted waveform is just a carrier tone,
$$x_z(t)=1$$
or
$$x_c(t)=\sqrt{2}\cos{(2\pi{f_c}t)}.$$
The received signal return at the radar receiver input has the form
$$
y_c(t)=A_P\sqrt{2}\cos{(2\pi(f_c+f_P)t+\theta_P)}+A_G\sqrt{2}\cos{(2\pi(f_c+f_G)t+θ_G)}
$$
where the P subscript refers to the signal returns from the plane taking off and the G subscript refers to the signal returns from the ground. The frequency shift is due to the Doppler effect you learned about in your physics classes.

**(a)** Why does the radar signal bouncing off the ground (obviously stationary) produce a Doppler frequency shift?

**(b)** Give the complex baseband form of this received signal.

**(c)** Assume the radar receiver has a complex baseband impulse response of
$$
h_z(t)=\delta(t)+\beta\delta(t-T)
$$
where $$\beta$$ is a possibly complex constant, find the value of $$\beta$$ which eliminates the returns from the ground at the output of the receiver.  This system was a common feature in early radar systems and has the common name Moving Target Indicator (MTI) as stationary target responses will be canceled in the filter given in Eq. (4.43).

Modern air traffic control radars are more sophisticated than this problem suggests. An important point of this problem is that radar and communication systems are similar in many ways and use the same analytical techniques for design.

![figure.03](hw03/hw03-fig03.png)


####3(a)


####3(b)


####3(c)
