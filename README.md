EXPT.NO: 6
SIMULATION OF AUTOCORRELATION AND PSD USING SCILAB

AIM:

To simulate and compute the Autocorrelation and Power Spectral Density (PSD) of a signal using SCILAB and to verify the Wiener–Khinchin relation.

EQUIPMENTS REQUIRED:

• Computer with i3 Processor
• SCILAB Software

THEORY:

Autocorrelation is a mathematical tool used to measure the similarity between a signal and a time-shifted version of itself. It provides information about repeating patterns and signal periodicity.

Power Spectral Density (PSD) describes how the power of a signal is distributed with frequency. It shows which frequency components contain most of the signal energy.

The Wiener–Khinchin Theorem states that:

ALGORITHM:

Define time vector for the signal.

Generate the input signal 𝑥(𝑡).

Compute Autocorrelation using xcorr() function.

Compute FFT of autocorrelation to obtain PSD.

Compute FFT of original signal and take magnitude square.

Plot all signals.

Compare both PSD results to verify Wiener–Khinchin theorem.

PROCEDURE:

• Refer Algorithm and write code for the experiment.
• Open SCILAB in System.
• Type the code in New Editor.
• Save the file.
• Execute the code.
• If any error occurs, correct and execute again.
• Verify the generated waveform using tabulation and model waveform.

PROGRAM:
`````
t=0:0.01:2*3.14
x=3*sin(3*t)
subplot(5,1,1);
plot(x);
au=xcorr(x,x);
subplot(5,1,2);
plot(au);
v=fft(au);
subplot(5,1,3);
plot(abs(v));
fw=fft(x);
subplot(5,1,4);
plot(fw);
fw2=(abs(fw)).^2;
subplot(5,1,5);
plot(fw2);
`````
OUTPUT WAVEFORM:
<img width="1912" height="1110" alt="image" src="https://github.com/user-attachments/assets/9570ca65-d624-4506-aa5a-a5aa4b40c12a" />


RESULT:

Thus, the Autocorrelation and Power Spectral Density of the given signal are successfully simulated using SCILAB.

The Wiener–Khinchin theorem is verified since the PSD obtained from the Fourier Transform of autocorrelation matches with the PSD obtained from the magnitude square of FFT of the signal.
