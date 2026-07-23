# Joystick-Cursor-Controller
A hardware-software bridge that transforms an analog 2-axis joystick into a fully functional desktop mouse cursor controller, using an Arduino to sample hardware inputs and a Python daemon to handle cross-platform OS-level mouse emulation.

---
## Demo
![Project Demo]

---
## Project Architechture
The project is split into two independent modules communicating over a shared Serial connection:
1. Firmware (/arduino): Samples the analog voltages from the X/Y potentiometer joystick axes and monitors the digital click state of the integrated select button. It packages these metrics into a lightweight serialized data string.
2. Software Daemon (/python): A background script that listens to the active COM port, deserializes the coordinates, translates the delta vectors, and injects native mouse events directly into the operating system window manager.
