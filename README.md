# SIMULATION-OF-AUTOCORRELATION-AND-PSD-USING-SCILAB-1-T1-C12-EVEN
AIM:

Write a program for Autocorrelation and PSD of signals in SCILAB and verify Wiener-Khinchin relation.

EQUIPMENTS Needed:

.Computer with i3 Processor

.SCI LAB

THEORY:

The Wiener-Khinchin theorem states that the power spectral density of a wide sense stationary random process is the Fourier transform of the corresponding autocorrelation function.

Algorithm:

1.Load or Define the Signal: Input your time-domain signal.

2.Compute Autocorrelation: Calculate the autocorrelation function of the signal.

3.Compute Power Spectral Density (PSD): Estimate the PSD of the signal, either directly using a method like Welch’s periodogram or by using the Fourier transform of the autocorrelation.

4.Plot Results: Visualize the autocorrelation function and PSD.

PROCEDURE:

Refer Algorithms and write code for the experiment.

Open SCILAB in System

Type your code in New Editor

Save the file

Execute the code

If any Error, correct it in code and execute again

Verify the generated waveform using Tabulation and Model Waveform

PROGRAM:

    clc;
    clear;
    close;
    
    // Step 1: Define signal
    t = 0:0.01:1;
    x = sin(2 * %pi * 5 * t);  // example signal
    
    // Step 2: Autocorrelation
    Rxx = xcorr(x);
    
    // Step 3: FFT
    X = fft(x);
    
    // Step 4: PSD
    PSD = abs(X).^2;
    
    // Frequency axis
    n = length(x);
    f = (0:n-1)/n;
    
    // -------- PLOTTING --------
    subplot(3,1,1);
    plot(t, x);
    title("Input Signal");
    
    subplot(3,1,2);
    plot(Rxx);
    title("Autocorrelation");
    
    subplot(3,1,3);
    plot(f, PSD);
    title("Power Spectral Density (PSD)");
OUTPUT:
<img width="940" height="556" alt="image" src="https://github.com/user-attachments/assets/0867da10-3c1c-45bb-ad17-955075a36c41" />


RESULT:
![20260406_181012](https://github.com/user-attachments/assets/232e4ad9-74d0-471a-a987-8a609b0c19f8)
