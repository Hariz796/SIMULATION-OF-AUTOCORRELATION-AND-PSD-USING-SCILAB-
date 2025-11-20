# SIMULATION-OF-AUTOCORRELATION-AND-PSD-USING-SCILAB-
## AIM
Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB

## THEORY
The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the Fourier transform of the corresponding autocorrelation function.
<img width="582" height="91" alt="image" src="https://github.com/user-attachments/assets/dacf7cfd-96c5-45a6-aa31-321978d15f97" />

## ALGORITHM
1.	Load or Define the Signal: Input your time-domain signal.
2.	Compute Autocorrelation: Calculate the autocorrelation function of the signal.
3.	Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like Welch’s periodogram or by using the Fourier transform of the autocorrelation.
4.	Plot Results: Visualize the autocorrelation function and PSD.

## PROCEDURE

•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated waveform using Tabulation and Model Waveform

## PROGRAM
```
clc;
clear;
t = 0:0.01:2*%pi;        // %pi is correct in Scilab
x = sin(2*t);

subplot(3,2,1);
plot(x);
title("Original Signal x(t)");

au = xcorr(x, x);        // Cross-correlation in Scilab
subplot(3,2,2);
plot(au);
title("Autocorrelation of x(t)");

v = fft(au);         // FFT (forward transform)
subplot(3,2,3);
plot(abs(v));
title("|FFT of Autocorrelation|");

fw = fft(x);
subplot(3,2,4);
plot(real(fw));
title("FFT of x(t) (Real Part)");

fw2 = (abs(fw)).^2;      // Power spectrum
subplot(3,2,5);
plot(fw2);
title("Power Spectrum |FFT(x)|^2");

```

## OUTPUT
<img width="1833" height="972" alt="image" src="https://github.com/user-attachments/assets/d9a6c221-2d7c-4529-835f-6629b96034d6" />


## RESULT`
Thus, the autocorrelation and PSD are executed in scilab and output is verified.

