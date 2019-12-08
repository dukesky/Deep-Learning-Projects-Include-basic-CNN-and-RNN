# This is STEP1

## Problem 1: Crowdsourcing a dataset of human-generated, random binary sequences

In this problem I will create an hdf5 file containing a numpy array of binary random sequences
that you generate yourself. Here are the steps to follow:

1. Obtain and run the template python file provided - this is in DEBUG mode by default.
2. Experiment with the error trapping assert statements to see what they are doing, using the
shape method on numpy arrays, etc.
3. Make the DEBUG flag False and enter 25 binary sequences, each of length 20. 
4. Make sure that hdf5 file has been written properly and can be read and checked to be
correct.

## Problem 2: Using Filters in Python
This is a basic problem to build prociency in Python. There are filter design and analysis tools
in Python that are very similar to those in Matlab. In this problem you will design and plot the
frequency response for a few ARMA lters. For your reference and review, Fig. 1.
1. Many methods in deep learning use a firrst order (L = 1) AR filter with unit gain at DC- 
i.e., the gain of the frequency response at zero frequency is 1. Also by "AR" it is implied that
b[i] = 0 for all i > 0. This type of lter has a single parameter \alpha which is the pole location
in the z-plane.
- (a) Specify the dierence equation and Z-transform for this rst order AR filter - i.e., specify
b[0], and a[1] in terms of \alpha. Note that, in the standard form in Fig. 1 a[0] = 1 by default,
but, just as in matlab, you need to enter for a[0] in the Python routine.
- (b) Plot the magnitude of the frequency response for \alpha = 0.9, \alpha = 0.5, \alpha = 0.1, \alpha = -0.5.
Use linear normalized frequency v, which is unique on [-1/2, +1/2] and has units of
cycles per sample. *Hint: use `scipy.signal.freqz`*.
![image1](../images/q2.png)
Figure 1: The general format and notation for an ARMA filter. The arrays of AR coefficients a[n]
and MA coefficients b[n] dene the filter. The order of teh filter is the number of delay elements in
this diagram, L.
- (a) If the time constant is dened as the number of samples required for the impulse response
to decay to 20 % of its value at n = 0, give the time constant for \alpha = 0.9, \alpha = 0.5, \alpha = 0.1.
- (b) Design an L = 4 Butterworth lter with bandwidth of v0 = 0.25. Provide the AR and
MA coeefficients and plot the magnitude of the frequency response.
- (c) Create a numpy array of length 300 comprising iid realizations of a standard normal
distribution. Filter this sequence using the Butterworth lter and plot the input and
output signals on the same plot. *Hint: Use `scipy.signal.lfilter`*.