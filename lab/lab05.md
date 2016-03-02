# lab05

## TITLE:
Central Limit Theorem (CLT)


##INTRODUCTION:
The central limit theorem (CLT) implies that the sum of arbitrarily distributed random variables tends to a Gaussian random variable as the number of terms in the sum gets large. Because many physical phenomena in communications systems are due to interactions of large numbers of events (e.g., random electron motion in conductors or large numbers of scatters in wireless propagation), this theorem is one of the major reasons why the Gaussian random variable is so prevalent in the communications system analysis. - *Fitz.* 3.3.5


##OBJECTIVES:
1. To understand why we use the Gaussian pdf so often in communication systems.
2. Use of MATLAB to complement this understanding.
3. Use of MATLAB to view some noise effects on signals.


##PRE-LAB:
1. Read ‘Random Variables’ (refer *Fitz* 3.2).
2. Read ‘Central Limit Theorem’ (refer *Fitz* 3.3.5).


## EQUIPMENTS:
1. MATLAB Software


##LAB:
- ####*Experimental proof using MATLAB:*
	1. In MATLAV, create a large array of random numbers that are uniformly generated ranging from -1:1 using the `rand()` function.
	2. Plot and view the distribution of these randomly generated numbers using the `hist()` function.
	3. If we then have many of these arrays, use the central limit theorem and MATLAB to simulate the sample distribution of the mean of the arrays. (**HINT**: you will need to use a new array of uniform random numbers for each sum).
	4. Again using the `hist()` function view this new distribution. What kind of distribution does it look like?

- ####*Noise corruption of a signal:*
	1. We have the information signal $$x(t)=\text{sinc}^2{(\pi{t})}$$ and we want to send it to a friend at a carrier frequency of $$20\:\text{Hz}$$. Draw the Fourier Transform of $$x(t)=\text{sinc}^2{(\pi{t})}\cos{(40\pi{t})}$$
	2. Using MATLAB, represent our information signal and plot it from time [-2:2]s
	3. Upconvert the info to our carrier frequency, plot this new signal and its Fourier Transform using `fft()`.
	4. While sending this signal to our friend it encounters noise in the channel. Using MATLAB’s `normrdn()` generate a Gaussian noise signal with $$\text{mean}=0$$, $$\text{variance}=.001$$ and a length the same as your information signal’s.
	5. Plot and view you’re the signal when your friend receives it, (after it encounters the noise) in the time and frequency domains.
	6. Plot and view the received signal in time and frequency when the channel noise has variance: 0.005, 0.01, 0.05.
