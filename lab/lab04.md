# lab04

## TITLE:
Noise in Communication Systems


## INTRODUCTION:
Noise in communication systems is produced from a filtering operation on wideband noise that appears as the receiver input. The input noise in a communication system is modeled as an additive white Gaussian noise. The white noise can come from a combination of the receiver electronics, human‐made noise sources or galactic noise sources.


## OBJECTIVES:
1. To use MATLAB and Simulink to look at how noise affects our signal quality.
2. To look at ways we can start to get back some of this quality.


## PRE-LAB:
1. Read ‘Thermal Noise’ (refer *Fitz* 9.4).
2. Read ‘Bandpass Random Processes’ (refer *Fitz* 10.1).


## EQUIPMENTS:
1. MATLAB and Simulink Software


## LAB:
1. Add noise to your previous MATLAB script for the amplitude modulated signal and filter it out in the demodulated signal.

2. MATLAB Code
	1. Load an audio file into you workspace using the `load()` function.
	2. Create a zero mean noise signal and add it to the music signal. (Start with zero variance and step up to a variance of 1 with at least 5 steps. Use either the `randn()` or `normrnd()` functions).
	3. Play the audio plus noise messages using the `sound()` function. You will need the sampling rate. Also plot them in time and view the plots.
	4. Make a table of noise variance versus audio quality (from excellent to atrocious).
	5. Pick a noise variance where the audio quality was fair to poor and work with this signal.
	6. View and compare your noisy signal and the original in the frequency domain.
	7. What can you do to your noisy signal in the frequency domain to decrease the noise power? Do it. (**HINT**: whatever you do to the signal must be done symmetrically to the fft for it to work when you reverse it back to time. Also do it to the actually `fft()` not the `abs(fft())`...)
	8. Once again play your message. How does it sound?
	9. Now open the filter GUI using the command `FDAtool`
	10. You can use this to create filter coefficients for a filter you design and then implement the filter using the `filter()` function.
	11. Implement a filter to do what you previously did with the `fft()` function
	12. How can you use these filters to act like an equalizer you see on a stereo?
	13. Try Bass or Treble Boosting the original music signal.

3. Simulink Model
	1. Create a Simulink model which has a speech signal. Corrupt it with noise and then reduce the noise by means of a filter. Use the blocks, ‘From Multimedia File’, ‘Noise’, ‘FDATool’ for Noise filter, ‘LMS Filter’, ‘Terminator’, ‘Product’, ‘Scope’, “On‐Off’, & ‘Terminator’.
	2. Observe the audio output at various points in the model (e.g. at the noise source, after the filter, the original signal and one corrupted by noise).
