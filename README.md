# Joystick-Cursor-Controller
A hardware-software bridge that transforms an analog 2-axis joystick into a fully functional desktop mouse cursor controller, using an Arduino to sample hardware inputs and a Python daemon to handle cross-platform OS-level mouse emulation.

---
## Demo
![Project Demo]

---
## How It Works
1) **Hardware Sampling Layer (Arduino C++)**
* **ADC Reading:**The dual axis potentiometers divide voltage between $0\text{V}$ and $5\text{V}$, mapped to 10-bit digital values (`0` to `1023`) via the Arduino's Analog-to-Digital Converter.

---
## 
