# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt


Am = 6.5
fm = 511
t = np.arange(0, 2/fm, 1/fs)

m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)

Ac = 13.0
fc = 5110
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)

B = 6.6
s = Ac * np.cos(2 * np.pi * fc * t + B * np.sin(2 * np.pi * fm * t))
plt.subplot(3, 1, 3)
plt.plot(t, s)

plt.tight_layout()
```
Output Waveform

<img width="1170" height="903" alt="Fm out" src="https://github.com/user-attachments/assets/415bd3ab-21cc-436f-9bfe-d58b67a3f03b" />


Tabular Column

![Fm modulation using python](https://github.com/user-attachments/assets/6a61bb88-154b-45ec-902a-2588b438049f)



Calculation

![Fm using python page 2](https://github.com/user-attachments/assets/5495b29f-e388-43cd-b643-7f4c17add4c4)



Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
