# Ideal, Natural, & Flat-top -Sampling
# Aim
Write a simple Python program for the construction and reconstruction of ideal, natural, and flattop sampling.
# Tools required
python IDE with Numpy and Scipy
# Program
```
import numpy as np
import matplotlib.pyplot as plt
from scipy.signal import resample
fs = 100
t = np.arange(0, 1, 1/fs) 
f = 5
signal = np.sin(2 * np.pi * f * t)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal')
plt.title('Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
t_sampled = np.arange(0, 1, 1/fs)
signal_sampled = np.sin(2 * np.pi * f * t_sampled)
plt.figure(figsize=(10, 4))
plt.plot(t, signal, label='Continuous Signal', alpha=0.7)
plt.stem(t_sampled, signal_sampled, linefmt='r-', markerfmt='ro', basefmt='r-', label='Sampled Signal (fs = 100 Hz)')
plt.title('Sampling of Continuous Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
reconstructed_signal = resample(signal_sampled, len(t))
plt.figure(figsize=(10, 4))
plt.plot(t, reconstructed_signal, 'r--', label='Reconstructed Signal (fs = 100 Hz)')
plt.title('Reconstruction of Sampled Signal (fs = 100 Hz)')
plt.xlabel('Time [s]')
plt.ylabel('Amplitude')
plt.grid(True)
plt.legend()
plt.show()
```
# Output Waveform

<img width="866" height="393" alt="image" src="https://github.com/user-attachments/assets/94d7620a-7356-4780-9b86-464e12802b5c" />

<img width="866" height="393" alt="image" src="https://github.com/user-attachments/assets/902bcacb-8134-42c8-82ef-e2ac9424a251" />

<img width="866" height="393" alt="image" src="https://github.com/user-attachments/assets/ecf1756d-90b3-4c45-a6d4-970ba0dc3cda" />


# Results

The Construction or Re-construction of impulse or ideal sampling using python are verified.

