java c
Elec4621 Lab Task 2 
This lab aims to cover the concepts of filtering and linear time-invariant systems. It will give you some exposure to the ways these systems are manipulated and allows you to develop some insight into their working.
1 Filters and Impulse Response 
The first part of the lab looks at filters. In particular you will consider an FIR in order to focus on the concepts of impulse response and transfer function. You will also apply the filter to real data and experiment with the location of its zeroes to achieve a particular response.
A fifth order all-zero filter has the following transfer function,

where

1. Find the impulse response of the filter.
Hint: There are a number of ways to do this: One way is to build a vector, v, containing all 5 zeroes, and then use the Matlab function, 'poly', to find the coefficients of the polynomial with these roots-the coefficients of the polynomial are the filter taps. Another way is to proceed from the second order sections of the transfer function and use polynomial multiplication to build 5-th order numerator. Then you will have the filter taps.
2. Find and plot the magnitude and phase responses of the filter.
Hint: You should remember that the frequency response is obtained by substituting z=ejw. Therefore you can think of this as the evaluation of the transfer function on a fine grid of w. Thus. you can construct a vector w of angular frequencies and evaluate the transfer function for this vector, then plot the amplitude and phase of the result.
3. Apply the filter to the sunspot data from the previous lab. What do you observe?
4. Suppose that we want to suppress the high frequency noise of the sunspot data to better see the 11 year and longer term cycles. Experiment with the zeros of the filter above to achieve this.
2 Sampling and Reconstruction 
This section of the lab deals with the concepts of sampling and reconstruction. In this lab you will focus on these concepts in order to verify and cement your understanding of how these ideas apply. You will employ the view of reconstruction as "joining the dots" in some way to understand how aliasing can be recruited to manipulate signals.
Consider the signal x(t) = Acos(wt) where A = 1 and ω = 2πf with f = 110 Hz. In the rest of this part, and unless otherwise specified, you are to plot the signals in the time for 0 ≤t< 30 ms and in the frequency domain for-1000
1. What is the minimum sampling frequency to a代 写Elec4621 Lab Task 2Matlab
代做程序编程语言void aliasing.
2. Suppose we sample the signal at fs = 300 Hz. Plot the continuous and sampled signals. Hint: To plot the continuous time signal use a very small time step (compared to the sampling time).
3. Plot the Fourier spectra of the continuous and sampled signals.
4. Show by examples that there are signals other than x(t) above that also go through the same set of samples. That is plot other signals that go through all of the samples. Comment on these signals: what form. do they have, what do they exhibit that is in common with the signal x(t) and with one another? What are the differences between them? How many of them are there?
5. Now suppose that we want to recover the continuous time signal. Give the specification of a suitable reconstruction filter to achieve this. Design a practical FIR filter to do the same.
6. Apply the filter to the sampled signal and plot and compare the original and reconstructed signals. Also plot and compare their spectra.
7. Now suppose that we want the reconstructed signal to have a frequency of 70 Hz. Suggest a way to achieve this via a suitable choice of the sampling frequency and reconstruction filter. Implement this system and plot and compare the original and reconstructed signals both in the time and frequency domains.
8. Now suppose that we want the reconstructed signal to have a frequency of 170 Hz. Repeat the previous part by suggesting a suitable choice of the sampling and reconstruction filter to achieve this.
3 Quantisation Effects 
In this part you will look at practical implementation issues of filters on real digital signal processors. This is a topic that we will cover in the lectures, so this lab exercise is ahead of the class. When a filter is implemented on a DSP, a binary representation of the various numbers (both the filter coefficients as well as the samples of the signals) is needed. Any binary representation has necessarily a finite bit depth and so the various quantities are quantised in the adopted representation. This quantisation leads to errors in the transfer function. Also errors in the samples of the signals at various points of the filter propagate and accumulate. This lab will expose you to some of these concepts.
A fourth order filter has the following poles and zeroes

and

1. What is the transfer function of the filter?
2. Plot the magnitude and phase responses of the filter.







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
