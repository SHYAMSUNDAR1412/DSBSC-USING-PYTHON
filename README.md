# DSBSC-USING-PYTHON
Aim

To implement and analyze Double Sideband Suppressed Carrier (DSB-SC) modulation using Python’s NumPy and Matplotlib libraries.

Apparatus Required

Software: Python with NumPy and Matplotlib libraries
Hardware: Personal Computer

Theory

Double Sideband Suppressed Carrier (DSB-SC) is a type of amplitude modulation where the carrier signal is suppressed, and only the sidebands (which contain the information) are transmitted.

<img width="864" height="538" alt="image" src="https://github.com/user-attachments/assets/38453f40-70c0-4697-b347-10cc10c0db6c" />


<img width="815" height="471" alt="image" src="https://github.com/user-attachments/assets/47223c8c-4587-402f-8703-3dccd7d8c4e8" />

PROGRAM:
```
import numpy as np
import matplotlib.pyplot as plt
Am = 5.4
Ac = 10.8
fm = 434
fc = 4340
fs = 43400
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
c = Ac * np.cos(2 * np.pi * fc * t)
s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)
s = s1 - s2
plt.figure(figsize=(10, 6))
plt.subplot(3,1,1)
plt.plot(t, m)
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.grid()
plt.subplot(3,1,2)
plt.plot(t, c)
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.grid()
plt.subplot(3,1,3)
plt.plot(t, s)
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.grid()
plt.tight_layout()
plt.show()
```
OUTPUT WAVEFORM:

<img width="989" height="590" alt="image" src="https://github.com/user-attachments/assets/f61dffd0-7d4b-4a96-86d7-f3ec0b99bd04" />

TABULATION:

![WhatsApp Image 2025-10-26 at 19 31 15_c5cae55f](https://github.com/user-attachments/assets/474ded22-8e9f-4945-a8ae-e161e561531f)

RESULT:

Thus, Double Sideband Suppressed Carrier (DSB-SC) modulation was successfully implemented using Python’s NumPy and Matplotlib libraries, and the message, carrier, and modulated waveforms were plotted and analyzed.



