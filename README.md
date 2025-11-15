# -Amplitude-Modulation-and-Demodulation-using-NumPy-and-Matplotlib
 # NAME : NABISHA A
# REG NO : 212223060177

__Aim__: 

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

__Apparatus Required__: 

Software: Python with NumPy and Matplotlib libraries 
Hardware: Personal Computer 

__Theory__: 

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting 
information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of 
the message signal. The general form of an AM signal is: 


__Algorithm__:
1. Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency. 
2. Generate Time Axis: Create a time vector for the signal duration. 
3. Generate Message Signal: Define the message signal as a cosine wave. 
4. Generate Carrier Signal: Define the carrier signal as a cosine wave. 
5. Modulate Signal: Apply the AM formula to obtain the modulated signal. 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

PROGRAM :
```
import numpy as np 
import matplotlib.pyplot as plt 
# Given parameters 
Ac = 7 # Carrier amplitude 
fc = 1200  # Carrier frequency in Hz 
Am = 5# Message signal amplitude 
fm = 120 # Message signal frequency in Hz 
fs = 12000  # Sampling frequency 
t = np.arange(0, 2/fm, 1/fs)  # Time vector 
# Message signal (modulating signal) 
Em = Am * np.sin(2 * np.pi * fm * t) 
# Carrier signal 
Ec = Ac * np.sin(2 * np.pi * fc * t) 
# Amplitude Modulated (AM) signal 
Eam = (Ac + Am * np.sin(2 * np.pi * fm * t)) * np.sin(2 * np.pi * fc * t) 
# Plot the signals 
plt.figure(figsize=(10, 6)) 
plt.subplot(3, 1, 1) 
plt.plot(t, Em) 
plt.grid() 
plt.subplot(3, 1, 2) 
plt.plot(t, Ec) 
plt.grid() 
plt.subplot(3, 1, 3) 
plt.plot(t, Eam) 
plt.grid() 
plt.tight_layout() 
plt.show()
```
__TABULATION__:
<img width="588" height="352" alt="image" src="https://github.com/user-attachments/assets/de31f9b6-8a27-4d0c-a684-3a47254c3d0b" />


__CALCULATION__:
<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/52e4ee41-4538-45ae-b5e8-f2d220cf69ef" />


 __Output__:
 
<img width="1080" height="1141" alt="image" src="https://github.com/user-attachments/assets/8a1e6987-088e-42f9-9039-44727a1b65b3" />


 __Result__:
The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. Thus, AM is implemented using numPy and Matplotlib.

